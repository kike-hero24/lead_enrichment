# Informe de enriquecimiento — 2026-11-04 · Lote 4 (modo real) — DETENIDO POR CONFLICTO

Lista: `supplier_acquisition_pipeline` · Checkpoint acumulado: `progress.json` (139 fichas) · Llamadas: `requiere_llamada.csv` (33)

## 1. Resoluciones aprobadas por el usuario (aplicadas antes del lote)

| Ficha | Qué se hizo |
|---|---|
| Aurelma S.L. Construcciones | Email corregido de raurelma@ a **aurelma@aurelma.es**. Teléfonos +34600488582 y +34923257693. Fuente y confianza Alta. Comentario |
| Construcciones González Salamanca | Teléfonos de la web: **+34605996624 / +34923252808**, que sustituyen al +34616486580 (anotado en un comentario). Persona info@construccionesgonzalez.com. Fuente y confianza Alta |
| 9 dominios propuestos | Ingrinamar, Ediglema, Reformas Integrales Alonso, Globalcons, Julián Hernández, Consan, Blázquez, Cotatres y Promantec24 |
| 5 emails | isabel@ediglema.es, hola@reformasalonso.es, info@construccionesconsan.com, info@construccionesblazquez.es y contacto@cotatres.es |
| 3 webs de captación descartadas | reformassalamanca.es, Pintor Salamanca y Jardineros Salamanca |

Las webs de captación tienen un comentario «DESCARTADA» en su entrada. No se modificó ni la etapa ni ningún otro dato.

## 2. Lote 4: selección y parada

Se seleccionaron 50 fichas de otras verticales, Tier 2, Salamanca, en *Prospect Discovery*: limpieza, jardinería, mudanzas, administradores de fincas, informática, piscinas, toldos y pintura. Se investigaron las 50.

**Parada en la ficha 19 (Toldos Moñita):** el dominio guardado (`toldossalamanca.es`) y el email (`info@toldossalamanca.es`) son de **otra empresa**, un instalador de toldos del barrio de Salamanca en Madrid. La web real de Toldos Moñita es **monita.es**:
- Delegación de Salamanca en el Pol. El Montalvo II.
- Teléfonos +34923190214 y +34923194224.
- Email salamanca@monita.es.

Se dejó un comentario en la entrada de la lista y no se modificó nada más. **No hubo errores de herramienta.**

**Hay otro conflicto ya detectado más adelante:** en **CUPOSOL** (ficha 31), el `phone_number_2` +34615113027 no aparece en la web. La web publica +34658855968 (móvil) y +34923204382.

Las fichas 20 a 50 **no están en `progress.json`** y entrarán en el siguiente lote. Su investigación está guardada en `investigacion_pendiente_lote4.md`, así que no hace falta repetirla.

## 3. Fichas procesadas (19)

### Enriquecidas (8)

| Ficha | Teléfonos escritos | Persona/email | Dominio | WhatsApp | Fuente |
|---|---|---|---|---|---|
| Tecnyvan | +34629889180 / +34923255352 (+ comentario con las delegaciones) | (ya existía) | — | **Sí** | https://tecnyvan.com/aviso-legal/ |
| LunaliaTech | +34624011939 | frankaquino@lunaliatech.com | lunaliatech.com | **Sí** | https://lunaliatech.com/legal/aviso-legal.html |
| Sucesores de Moreno | +34923226886 / +34923223134 (+ comentario con Badajoz) | (ya existía) | — | No | https://sucesoresdemoreno.com/136-2/ |
| Falken Informática | p2 +34640512782 (p1 ya coincidía) | — | — | No | https://www.falkeninformaticasalamanca.com/find-us |
| MAN&MAN | +34622718098 | (ya existía) | — | No | https://manyman.es/contacto |
| Mudanzas y Transportes Tormes | +34626404041 / +34923253459 | — | mudanzastormessalamanca.com | No | https://www.mudanzastormessalamanca.com/ |
| Artista García | — (ya coincidía) | hola@artistagarcia.com | — | No | https://artistagarcia.com/contacto/ |
| Móvilnext | +34634696645 | (ya existía) | — | No | https://www.movilnext.es/contacto/ |

### Requieren llamada (9)

| Ficha | Motivo |
|---|---|
| Pinturas BarGom | sin web |
| Jardinería Salamanca Verde | sin web |
| Gesmar | identidad dudosa: solo hay una Gesmar registrada, en Madrid |
| Multiservicios EDUCE | sin web; actividad dudosa |
| Jardinería El Manzano | sin web; posible cierre |
| Tot-Net | web 403; empresa nacional; **sin teléfono** |
| Vanessa Blanco Casado | la web no resuelve |
| Administraciones Castro Blanco | sin web |
| Pinturas Bragado | web 503 |

### Otras (2)

- **Retenida (intermediario):** Centro Reto Salamanca / El Recogedor. `centroretosalamanca.es` es una web de captación con titular en Córdoba que desvía las llamadas a otro profesional. Puede ser un uso indebido de la marca de la ONG.
- **Conflicto:** Toldos Moñita (ver arriba).

## 4. Problemas detectados (solo se informan)

- **Fichas contaminadas por un enriquecimiento automático erróneo:**
  - **Jardinería El Manzano** tiene el dominio `facebook.com` y los datos de Meta (Menlo Park, más de 10.000 empleados).
  - **SERVIS Salamanca** (ficha 34, pendiente) tiene el dominio `squarespace.com` y datos de Squarespace (New York).
  - Conviene limpiarlas a mano.
- **Fuera de servicios del hogar:** informática (Falken, Móvilnext, LunaliaTech), restauración de arte (Artista García) y transporte de arte (Mudanzas Feltrero, pendiente). Conviene revisar si deben seguir en la lista.
- **Tecnyvan:** la `primary_location` de la ficha no coincide con las direcciones de la web.

## 5. URLs usadas (fichas escritas)
https://tecnyvan.com/aviso-legal/ · https://tecnyvan.com/en/where-are-we-based/ · https://lunaliatech.com/legal/aviso-legal.html · https://sucesoresdemoreno.com/136-2/ · https://www.falkeninformaticasalamanca.com/find-us · https://manyman.es/contacto · https://www.mudanzastormessalamanca.com/ · https://artistagarcia.com/contacto/ · https://www.movilnext.es/contacto/ · https://monita.es/

## Cierre

- **Procesadas:** 19 (de las 50 seleccionadas; detenido por conflicto)
- **Con dato escrito:** 8
- **Sin dato:** 11
  - 9 pasan a llamada
  - 1 retenida
  - 1 conflicto
- **Pasan a llamada:** 9 (1 de ellas sin ningún teléfono)

**Slack:** Enriquecimiento 04/11 (lote 4): resoluciones aplicadas (Aurelma, Construcciones González, 9 dominios, 3 descartes). Lote detenido en la ficha 19 por conflicto en Toldos Moñita (dominio de otra empresa) → 19 procesadas, 8 con dato, 9 a llamada; 31 investigadas pendientes (otro conflicto ya detectado: CUPOSOL).
