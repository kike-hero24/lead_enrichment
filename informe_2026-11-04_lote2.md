# Informe de enriquecimiento: 2026-11-04, lote 2 (modo real), DETENIDO POR CONFLICTO

Lista: `supplier_acquisition_pipeline`. Checkpoint acumulado en `progress.json` (46 fichas). Fichas para llamar en `requiere_llamada.csv`.

## ⚠️ Motivo de la parada

En la ficha 6 del lote (**Aurelma S.L. Construcciones**) el dato de Attio no coincide con el de la web:
- **En Attio:** la persona de `team` tiene el email `raurelma@aurelma.es`.
- **En la web propia** (https://www.aurelma.es/contacto/)**:** solo aparece `aurelma@aurelma.es` en el HTML. La «r» del dato de Attio parece un resto del icono que se coló al extraer el texto renderizado. Es probable que el email guardado sea erróneo.
- **Lo que hice:** dejé un comentario en la entrada de la lista con el dato nuevo, la URL y la fecha. No modifiqué nada más, ni siquiera los teléfonos de esta ficha, que estaban vacíos: +34600488582 y +34923257693.

Me detuve aquí, como pediste. No hubo errores de herramienta.

**Más adelante en el lote hay otro conflicto, sin tocar:** en **Construcciones González Salamanca** (ficha 26), el teléfono de Attio +34616486580 no aparece en su web. La web publica +34605996624 (móvil, con WhatsApp) y +34923252808 (aviso legal de Construcciones González Salamanca SL, B37321510).

## Selección del lote

Reformas Tier 2 de Salamanca (21) + Reformas Tier 3 de Salamanca (12) + 7 de otras verticales con Tier 2.

Todas las de Reformas en Málaga ya tienen Fuente y Confianza, así que se saltaron. Las 40 fichas están investigadas, pero **solo se escribieron las 6 primeras**. Las otras 34 no están en `progress.json` y entrarán en el siguiente lote.

## Fichas procesadas (6)

| # | Ficha | Resultado | Escrito en Attio | WhatsApp en la web | Fuente |
|---|---|---|---|---|---|
| 1 | Ingrinamar (Limpiezas y reformas) | Enriquecida | phone_number +34615635128 · fuente · confianza Alta | **Sí** (api.whatsapp 34615635128) | https://www.ingrinamar.es/es/contacto/ |
| 2 | Reformas Reis | Requiere llamada | — | — | Web caída (503) |
| 3 | Construcciones Reformas y Servicios San Agustín | Requiere llamada / propuesta | — | — | No se confirma que la web sea suya |
| 4 | Oyrsa Constructora | Enriquecida | phone_number_2 +34626055592 · persona info@oyrsa.es · fuente · confianza Alta | El enlace del pie apunta a +34926655592 (errata) | https://oyrsa.es/contacto/ |
| 5 | Reformálitas | Enriquecida | phone_number_2 +34638459948 · persona info@reformalitas.es · comentario con el 902 36 36 36 · fuente · confianza Alta | No | https://reformalitas.es/contacto/ |
| 6 | Aurelma S.L. Construcciones | **Conflicto** | Solo el comentario | No | https://www.aurelma.es/contacto/ |

- **Teléfonos añadidos:** 3. Ninguno sobrescrito: Oyrsa y Reformálitas ya tenían `phone_number`, que coincide con la web.
- **Personas/emails creados:** 2, en empresas cuyo dominio ya coincidía con el del email, para que Attio no cree empresas duplicadas.
- **Dominios añadidos:** 0.
- **Comentarios:** 2 (el 902 de Reformálitas y el conflicto de Aurelma).

### Propuestas que no se escribieron
- **Ingrinamar:** el dominio `ingrinamar.es` queda como propuesta. Solo hay coincidencia de nombre: la web no indica ciudad (salvo el mapa) y la ficha no tenía teléfono con el que comparar.
- **San Agustín:** la web `reformasyserviciossanagustin.com` muestra el nombre «Reformas y Servicios San Agustín», sin ciudad. Su teléfono (+34645989988) es distinto al de Attio, y el email es de Gmail (`reformas.sanagustin@gmail.com`). No hay identidad clara.

## Problemas detectados (solo se informan)
- **Oyrsa:**
  - Las coordenadas son genéricas (40.4637, -3.7492).
  - Es un grupo grande (más de 90 empleados, oficinas en Madrid y Tenerife), no un pequeño profesional.
  - El enlace de WhatsApp del pie tiene una errata.
- **Reformálitas:** el titular de la web es una sociedad portuguesa (Brisas Manuscritas Unipessoal LDA). Es una red con oficinas en Salamanca, Pontevedra, Alicante y Covilhã.
- **Aurelma:** el aviso legal no tiene CIF.

## Investigadas pero sin escribir (34). Pendientes para el siguiente lote

Resumen de lo que encontraron los agentes. **No se ha escrito nada**: se aplicará en el siguiente lote con las reglas vigentes.

- **Con web propia y datos verificables (≈22):**
  - Jomisaga (reformasjomisaga.es)
  - Luxury Design (3 teléfonos)
  - DICAL (WhatsApp)
  - Home Projects
  - Mavisal (el aviso legal es una plantilla del desarrollador)
  - Jimeya (WhatsApp)
  - Azugres
  - Globalcons
  - Vika Interiorismo
  - Inter (email de Gmail; varias empresas homónimas)
  - Julián Hernández (autónomo, email de Gmail)
  - Consan (razón social Pavimentos Consan S.L.)
  - Blázquez
  - Cotatres
  - Diseño y Obra (**aviso legal plantilla con CIF B12345678 y dirección inventada**)
  - Hijos de Luis Martín García (teléfono coincide)
  - Construcciones 360 (teléfono coincide)
  - Ediglema
  - A Tu Modo Reforma
  - PHONEGAME
  - Reformas Salamanca/Promantec24: misma empresa que electricistasalamanca.es, con el mismo +34609142188 y WhatsApp
  - reformassalamanca.es: sin aviso legal ni CIF, posible web de captación
- **Conflicto ya detectado:** Construcciones González Salamanca (ver arriba).
- **Sin web propia o web inaccesible (a llamar en el siguiente lote):**
  - Reformas Integrales Alonso: su web está en Santa Marta de Tormes, ciudad no exacta
  - Herfoncal: el dominio no resuelve
  - Reformas El Mono
  - Salmantina Reformas: dominio **en venta**
  - Cocinas y Reformas Azuvi
  - Reparación de Electrodomésticos: nombre genérico; su teléfono parece de relleno
  - Florentino Cortés
  - Limpiezas Sillero: web 503
  - Limpiezas Duende: **el dominio `webs.com` es de Vistaprint**
  - Guijo y Serna: la web carga por JavaScript y no se pudo leer
  - AMANA: probable intermediario

## URLs usadas (fichas escritas)
https://www.ingrinamar.es/es/contacto/ · https://oyrsa.es/contacto/ · https://oyrsa.es/aviso-legal/ · https://reformalitas.es/contacto/ · https://reformalitas.es/aviso-legal/ · https://www.aurelma.es/contacto/ · https://www.aurelma.es/aviso-legal/

## Cierre

- **Procesadas:** 6 (de las 40 seleccionadas; detenido por conflicto)
- **Con dato escrito:** 3 (Ingrinamar, Oyrsa, Reformálitas)
- **Con dato encontrado pero sin escribir por conflicto:** 1 (Aurelma)
- **Sin dato:** 2 (Reformas Reis, San Agustín)
- **Pasan a llamada:** 2 (en `requiere_llamada.csv`)

**Slack:** Enriquecimiento 04/11 (lote 2): detenido en la 6ª ficha por conflicto de email en Aurelma → 6 procesadas, 3 con dato (3 tel., 2 emails), 2 a llamada, 1 conflicto; 34 investigadas pendientes de escribir (otro conflicto ya detectado en Construcciones González).
