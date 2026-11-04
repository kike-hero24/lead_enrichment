# Informe de enriquecimiento — 2026-11-04 · Lote 4 (modo real) — COMPLETADO

Lista: `supplier_acquisition_pipeline` · Checkpoint acumulado: `progress.json` (170 fichas) · Llamadas: `requiere_llamada.csv` (44)

> El lote se detuvo en la ficha 19 por conflicto (Toldos Moñita). Tras tu aprobación («pon los datos de la web») se resolvieron Moñita y CUPOSOL y se completaron las fichas 20-50. Ver sección 6.

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

## 6. Reanudación tras aprobación (fichas 19-50)

### Conflictos resueltos con tu aprobación

**Toldos Moñita**
- Dominio cambiado de `toldossalamanca.es` a **monita.es**.
- La persona `info@toldossalamanca.es`, de otra empresa, se ha **desvinculado** de la ficha. No se ha borrado.
- Añadidos `salamanca@monita.es` y los teléfonos +34923190214 / +34923194224.
- Comentario en la entrada.
- ⚠️ Al cambiar el dominio, el enriquecimiento automático de Attio rellenó la `primary_location` con **Coslada (Madrid)**, que es la sede central. `primary_city` sigue siendo Salamanca.

**CUPOSOL**
- Teléfonos de la web +34658855968 / +34923204382, que sustituyen al +34615113027.
- El número anterior queda en un comentario.

### Enriquecidas (20, incluidas las dos anteriores)

| Ficha | Teléfonos escritos | Persona/email | Dominio | WhatsApp |
|---|---|---|---|---|
| Toldos Moñita | +34923190214 / +34923194224 | salamanca@monita.es | monita.es (cambiado) | No |
| Mudanzas A. Alonso | +34659767124 | (ya existía, hotmail) | propuesta: mudanzasaalonso.es (Carbajosa) | No |
| Persianas Ruano Monzón | +34923233808 / +34923228299 | (ya existía) | — | No |
| SEILA | p1 +34923203529 (p2 ya coincidía) | (ya existía) | — | **Sí** |
| Limpieza General Salamanca | +34657126616 / +34923096243 | (ya existía, gmail) | limpiezageneralsalamanca.es | No |
| Gestión VUT Salamanca | p2 +34682700275 (p1 ya coincidía) | info@gestionvutsalamanca.com | gestionvutsalamanca.com | No |
| Limpiezas Mar Cabezas | +34923264139 | (ya existía, gmail) | limpiezasmarcabezassl.com | No |
| Factoría PC | p2 +34644561930 (p1 ya coincidía) | — (info@factoriapc.com, otro dominio) | — | indicado en texto |
| CUPOSOL | +34658855968 / +34923204382 | (ya existía) | — | No |
| LuPagest | +34679956111 / +34923175427 | (ya existía) | propuesta: lupagestsalamanca.es (ya tiene .com) | No |
| Helsein | +34661955885 / +34610264568 (+ comentario con el 24 h) | (ya existía) | — | **Sí** |
| Grupo CAB | +34923188453 | (ya existía) | — | No |
| PROMOTECH | +34923999500 | (ya existía) | — | **Sí** (sobre un fijo) |
| J. Mediero | +34686226472 | (ya existía) | — | No |
| Azor Limpiezas | p2 +34685105336 (p1 ya coincidía) | azor@azorlimpiezas.com | — | **Sí** |
| Aloja Salamanca | — (ya coincidía) | (ya existía) | — | No |
| Ibergarden | — (ya coincidía; comentario con los móviles de Segovia) | (ya existía) | — | No |
| Mudanzas Salamanca CYL | +34642236559 | (ya existía, gmail) | mudanzassalamancacyl.com | **Sí** |
| Adap Informática | p2 +34692635851 (p1 ya coincidía) | comercial@adap.es | — | No |
| Limpiezas García Hernández | +34676030634 | — (gmail) | propuesta: limpiezasgarciahernandez.com (Villamayor) | No |

Las fuentes de cada una son las URLs de contacto o aviso legal de su web.

### Requieren llamada (11)

| Ficha | Motivo | Teléfono en Attio |
|---|---|---|
| TODO EN CASA | el dominio no resuelve | Sí |
| Kevin Jardinería | la web no resuelve | **No** |
| SOQUIMSA | web 503 | **No** |
| Jardinería Monte Nuevo | web ilegible (carga por JavaScript) | Sí |
| María Vázquez Jiménez | sin web | Sí |
| SERVIS Salamanca | sin web; ficha contaminada con datos de Squarespace | Sí |
| Adm. Fincas María José Navarro | la web no resuelve | Sí |
| Administración de Fincas 1992 | sin web | **No** |
| Ape Colorado | su web no publica teléfono | Sí |
| MultiManitas | solo Instagram | **No** |
| M.ª Victoria Miguel Andrés | web 503 | Sí |

### Retenida (1)

- **Mudanzas Feltrero:** feltrero.com es de Feltrero División Arte S.L., que hace transporte de obras de arte y museografía, no mudanzas domésticas. No escribí nada. Hay que revisar si es un lead válido.

### Problemas detectados en la reanudación

- **Ubicaciones erróneas:**
  - Toldos Moñita: Coslada, por el enriquecimiento automático.
  - Azor Limpiezas: Zamora, aunque la web dice Salamanca.
  - Helsein: coordenadas genéricas 40.4637, -3.7492.
- **Posible misma titularidad** entre TODO EN CASA y Limpieza General Salamanca: misma dirección, Pl. Mirto 1, según los buscadores.
- **Fuera de servicios del hogar:** Aloja Salamanca y Gestión VUT (alquiler turístico), Ibergarden (multisede, con base en Segovia y Madrid), Grupo CAB, PROMOTECH, Adap y Factoría PC (informática).

## Cierre del lote 4 completo

- **Procesadas:** 50
- **Con dato escrito:** 28 (incluidos los 2 conflictos resueltos con tu aprobación)
- **Sin dato:** 22
  - 20 pasan a llamada
  - 2 retenidas (Centro Reto y Mudanzas Feltrero)
- **Pasan a llamada:** 20 (5 de ellas sin ningún teléfono)

**Totales del lote:**
- **Teléfonos añadidos:** 35. Se sustituyeron 2 con tu aprobación (CUPOSOL y Moñita).
- **Personas/emails creados:** 6.
- **Dominios:** 7 (uno de ellos cambiado).
- **Errores:** 0. Un fallo puntual de Attio en Aloja se resolvió al reintentar.

**Slack:** Enriquecimiento 04/11 (lote 4): 50 fichas → 28 con dato (35 tel., 6 emails, 7 dominios; Moñita y CUPOSOL resueltos con tu OK), 20 a llamada (5 sin teléfono), 2 retenidas; 0 errores.
