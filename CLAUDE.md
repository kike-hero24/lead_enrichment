# Enriquecimiento automático de leads (Hero24 · Attio)

Guarda este archivo como `CLAUDE.md` en una carpeta de trabajo (por ejemplo `~/hero24-enrichment/`) y lanza Claude Code desde ella.

## 0. Preparación (una sola vez)

1. Instala Claude Code y conecta Attio como servidor MCP:
   ```
   claude mcp add --transport http attio https://mcp.attio.com/mcp
   ```
   Dentro de Claude Code ejecuta `/mcp` y completa el login de Attio con una cuenta con permisos de escritura en el workspace **Hero24**.
2. Comprueba la conexión pidiendo: «Ejecuta whoami en Attio». Debe devolver el workspace `hero-24`.
3. (Opcional) Copia la skill `agency-agents` a `~/.claude/agents/` y usa los agentes *Sales Data Extraction Agent* y *Data Consolidation Agent*.
4. Prueba primero en **modo simulación** (sección 7) con 10 leads antes de dejarlo escribir.

## 1. Objetivo

Completar teléfono, email y fuente de los leads de la lista `supplier_acquisition_pipeline` (≈669 fichas) usando **solo datos publicados por el propio negocio en su web**, y dejar cada dato con su fuente y su nivel de confianza. No se contacta a nadie desde este proceso.

## 2. Estructura de Attio (ya existente, no la modifiques)

- **Lista**: `supplier_acquisition_pipeline` (padre: `companies`).
  - Atributos de entrada de lista: `phone_number`, `phone_number_2` (teléfonos), `stage`.
  - Etapas: Prospect Discovery → Qualification → Prioritization → Outreach → Follow-up → Negotiation → Contract → Onboarding → Activation.
- **Empresa (`companies`)**: `name`, `domains`, `service_verticals`, `primary_city`, `tier`, `whatsapp_disponible`, `fuente`, `confianza_del_dato` (Alta/Media/Baja), `google_resenas_no`, `scraped_rating`, `team` (personas).
- **Persona (`people`)**: `email_addresses`, `company`.
- Los comentarios de la entrada de lista (`list-comments`) contienen el estado de contacto («email enviado», «contactar por whatsapp», «llamar por teléfono»). Léelos, no los borres ni los contradigas.

## 3. Qué leads procesar

Procesa solo fichas en etapa **Prospect Discovery o Qualification** que cumplan alguna de estas condiciones:
- No tienen `phone_number` en la entrada de lista.
- No tienen ninguna persona con email en `team`.
- `fuente` está vacío, contiene un email, o `confianza_del_dato` está vacío.

Orden: primero verticales en este orden de prioridad → Fontanería, Electricista, Climatización, Reformas, resto. Dentro de cada una, Tier 1 y 2 antes que Tier 3.
Tamaño de lote: **40 fichas por ejecución**. Guarda un checkpoint en `progress.json` (ids ya procesados) para no repetir.

## 4. Método de búsqueda por ficha

1. **Si la empresa tiene `domains`**: busca `web_search` con **solo el dominio** (ej. `fontaco.com`) en modo `extended`. Esta forma devuelve la página de contacto del propio negocio; las búsquedas con palabras devuelven directorios con ruido.
2. **Si no tiene dominio** (frecuente en Salamanca): busca `"<nombre comercial> <ciudad>"` en modo `extended`, localiza su web propia y, solo si es inequívocamente la misma empresa (mismo nombre y ciudad), usa esa web.
3. Abre con `web_fetch` la página de contacto / aviso legal / pie de página de **la web propia**.
4. Extrae: teléfonos, email de contacto, y si hay botón o enlace de WhatsApp.

## 5. Reglas de escritura (criterio aprobado)

**Se escribe directamente, sin pedir permiso**, solo si el dato aparece en la web propia del negocio:
- `phone_number` / `phone_number_2`, siempre en formato `+34XXXXXXXXX` (9 dígitos tras el prefijo). Prioriza móviles (6xx, 7xx) en los dos campos. Si hay más de dos teléfonos (o un fijo extra), dejalo en un **comentario** de la entrada de lista.
- Email: crea o localiza la persona con `upsert-record` sobre `people` usando `email_addresses` como atributo de coincidencia, enlazada con `company`. Nunca crees una persona sin comprobar antes si ya existe.
- `fuente` = URL exacta de la página donde está el dato. `confianza_del_dato` = **Alta**.

**NO se escribe como dato fiable** (déjalo en el informe como «propuesta»):
- Datos que solo aparecen en directorios (Cylex, Páginas Amarillas, Empresite, etc.) → como mucho `Baja` y solo si el usuario lo aprueba.
- Teléfonos o emails que se contradicen entre fuentes.
- Emails «adivinados» por patrón (`nombre@dominio`). **Prohibido.**

**Nunca toques**: `stage`, `tier`, `whatsapp_disponible`, comentarios existentes, `name`, ni borres nada. La verificación de WhatsApp la hace el equipo en la llamada.

**Si el dato ya existe y es distinto**: no lo sobrescribas; añade un comentario con el dato nuevo, la URL y la fecha, y márcalo en el informe como «conflicto».

## 6. Detección de problemas (solo informar, no corregir)

Añade al informe, sin modificar: valoraciones `scraped_rating` > 5; ubicación fuera de España; coordenadas genéricas (40.46, -3.74); fichas con CIF de aspecto inventado o dominio «en venta»; teléfonos sin prefijo; emails de otro dominio distinto al de la web.

## 7. Modo simulación y ejecución

- **Simulación** (`DRY_RUN=1`): no escribas en Attio. Genera `propuestas.csv` con columnas: `record_id, nombre, campo, valor_actual, valor_propuesto, url_fuente, confianza`.
- **Ejecución real**: aplica las reglas de la sección 5 y genera `informe_YYYY-MM-DD.md`.

Ejemplo de ejecución desatendida (sin interfaz):
```
claude -p "Lee CLAUDE.md y procesa el siguiente lote de 40 fichas en modo real. Actualiza progress.json y genera el informe del día." \
  --permission-mode acceptEdits --allowedTools "mcp__attio__*" "WebSearch" "WebFetch" "Read" "Write"
```
Programación diaria (cron, 08:00):
```
0 8 * * 1-5 cd ~/hero24-enrichment && claude -p "Procesa el siguiente lote de 40 fichas (CLAUDE.md)." --permission-mode acceptEdits --allowedTools "mcp__attio__*" "WebSearch" "WebFetch" "Read" "Write" >> logs/$(date +\%F).log 2>&1
```
Ajusta los nombres de las herramientas MCP (`/mcp` los muestra) y revisa los permisos antes de dejarlo desatendido.

## 8. Informe diario (`informe_YYYY-MM-DD.md`)

Incluye: fichas procesadas; teléfonos añadidos; personas/emails creados; fichas sin dato encontrado; conflictos; problemas de la sección 6; fichas que requieren llamada porque la web no publica teléfono; lista de URLs usadas. Termina con un resumen de una línea para pegar en Slack.

## 9. Límites y cumplimiento

- Solo datos profesionales publicados por el negocio. No uses datos personales de redes sociales ni de registros mercantiles de personas físicas.
- Muchos fontaneros son autónomos: sus datos son personales a efectos del RGPD. Confirma con el DPO la base legal del contacto en frío y el mecanismo de baja antes de escalar.
- Respeta los límites de la web: no hagas más de 1 petición por segundo al mismo dominio.
- Si algo falla (permiso de Attio, límite de búsquedas), **detente**, guarda el checkpoint y deja constancia en el informe. No reintentes en bucle.

## 10. Siguiente fase (cuando el enriquecimiento esté estable)

1. Tier automático con criterios explícitos (reseñas, valoración, nº de técnicos, cobertura, dato completo).
2. Tareas de llamada en Attio con guion para Tier 1 (`create-task`).
3. Borradores de email en Gmail para el resto, con revisión humana antes de enviar.
4. Informe semanal de embudo con `run-basic-report` (contactados, respuestas, perfiles creados, Heroes con primer trabajo).
