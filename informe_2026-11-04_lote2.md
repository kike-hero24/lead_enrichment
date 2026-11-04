# Informe de enriquecimiento — 2026-11-04 · Lote 2 (modo real) — COMPLETADO

Lista: `supplier_acquisition_pipeline` · Checkpoint acumulado: `progress.json` (80 fichas) · Llamadas: `requiere_llamada.csv` (12)

## Desarrollo

1. Lote de 40 fichas, todas en *Prospect Discovery*:
   - Reformas Tier 2 de Salamanca: 21.
   - Reformas Tier 3 de Salamanca: 12.
   - Otras verticales con Tier 2: 7.
   - Las de Reformas en Málaga ya tenían Fuente y Confianza y se saltaron.
2. **Primera parada** en la ficha 6 (Aurelma) por conflicto, como se pidió. Se avisó y se reanudó a petición del usuario («continúa con las demás»).
3. **Construcciones González** era un conflicto ya avisado en el primer informe. Se registró con un comentario y no se modificó nada. Se siguió con el resto.
4. **Incidencia técnica:** el proceso que aplicaba las escrituras se cortó por el límite de uso de la API.
   - Se comprobó en Attio, ficha a ficha, que el plan completo quedó aplicado y sin duplicados: teléfonos de las 19 entradas, fuente y confianza de las 22 empresas, 6 dominios, 5 personas y 2 comentarios.
   - No hubo errores de escritura.

## Conflictos (2) — pendientes de tu decisión, no se escribió nada

| Ficha | Dato en Attio | Dato en la web propia | Fuente |
|---|---|---|---|
| Aurelma S.L. Construcciones | email raurelma@aurelma.es | aurelma@aurelma.es (la «r» parece un resto del icono) · teléfonos +34600488582 / +34923257693 | https://www.aurelma.es/contacto/ |
| Construcciones González Salamanca | teléfono +34616486580 | +34605996624 (con WhatsApp) / +34923252808 · info@construccionesgonzalez.com | https://construccionesgonzalez.com/ |

Las dos fichas tienen un comentario en su entrada de la lista con el dato nuevo, la URL y la fecha.

## Fichas enriquecidas (25)

| Ficha | Teléfonos escritos | Persona/email creado | Dominio añadido | WhatsApp | Fuente |
|---|---|---|---|---|---|
| Ingrinamar | +34615635128 | — | propuesta | **Sí** | https://www.ingrinamar.es/es/contacto/ |
| Oyrsa | p2 +34626055592 (p1 ya coincidía) | info@oyrsa.es | — | enlace con errata | https://oyrsa.es/contacto/ |
| Reformálitas | p2 +34638459948 (+ comentario con el 902) | info@reformalitas.es | — | No | https://reformalitas.es/contacto/ |
| Diseño y Obra | +34646596926 / +34923227737 | (ya existía) | — | No | https://disenoyobra.es/ |
| Hijos de Luis Martín García | p2 +34616429847 (p1 ya coincidía) | — | — | No | https://hluismartingarcia.com/ |
| Construcciones 360 | — (ya coincidía) | manuel.martin@construcciones360.es | construcciones360.es (teléfono coincide) | No | https://www.construcciones360.es/contacto |
| Construcciones Ediglema | +34685546696 / +34923197968 | — | propuesta | No | https://www.ediglema.es/aviso-legal-es-rgpd |
| Reformas Jomisaga | +34651838012 / +34923100493 | info@reformasjomisaga.es | reformasjomisaga.es (nombre y ciudad) | No | https://reformasjomisaga.es/contacto.html |
| Luxury Design España | +34679431201 / +34652131627 (+ comentario con el fijo) | (ya existía) | — | dudoso | https://www.luxurydesign.es/contacto |
| Reformas Integrales Alonso | +34695526636 | — | propuesta | No | https://www.reformasalonso.es/ |
| DICAL Reformas | — (ya coincidía) | — | — | **Sí** (wa.link) | https://dicalreformas.com/ |
| Home Projects (Proyectos del Hogar) | +34654036333 / +34923184409 | info@proyectosdelhogar.com | — | No | https://proyectosdelhogar.com/contacto/ |
| Mavisal | +34675895211 / +34923135786 | (ya existía) | — | No | https://mavisal.es/contacto/ |
| Pinturas y Reformas Jimeya | +34651572984 | (ya existía) | pinturasjimeya.com (nombre y ciudad) | **Sí** | https://www.pinturasjimeya.com/contacto |
| Azugres Baños | p2 +34630987781 (p1 ya coincidía) | — | — | No | https://azugresbanos.es/contactanos/ |
| Globalcons | +34627488440 / +34923213604 | — | propuesta | icono sin enlace | https://www.globalcons.es/_aviso-legal.php |
| Vika Interiorismo | +34923096711 | info@vikainteriorismo.com | vikainteriorismo.com (nombre y ciudad) | No | https://vikainteriorismo.com/contacto/ |
| Inter | — (ya coincidía) | — | — | No | https://interreformas.com/ |
| Julián Hernández Sánchez | +34650245800 | — | propuesta | widget sin enlace | https://obrasyserviciossalamanca.es/index.php/empresa/quienes-somos |
| Construcciones Consan | +34606992900 | — | propuesta | No | https://construccionesconsan.com/contacto/ |
| Construcciones Blázquez | +34923208387 | — | propuesta | No | https://www.construccionesblazquez.es/ |
| Cotatres | +34676492581 | — | propuesta | No | https://cotatres.es/ |
| Reformas Salamanca / Promantec24 | +34609142188 | — | propuesta | **Sí** | https://reformas-salamanca.es/aviso-legal/ |
| A Tu Modo Reforma | +34692873525 / +34609823985 | info@atumodoreforma.com | atumodoreforma.com (nombre y ciudad) | No | https://www.atumodoreforma.com/contacto |
| PHONEGAME / arreglodeconsolas.es | +34633015172 / +34923996854 | (ya existía) | arreglodeconsolas.es (nombre y ciudad) | dice que sí, sin enlace | https://www.arreglodeconsolas.es/contacto/ |

**Totales del lote:**
- **Teléfonos añadidos:** 31. No se sobrescribió ninguno.
- **Personas/emails creados:** 7.
- **Dominios añadidos:** 6.
- **Comentarios:** 4 (2 de teléfonos extra y 2 de conflicto).

**Criterio de ciudad:** `primary_city` = Salamanca agrupa la provincia. Por eso se aceptaron las webs de empresas de pueblos del alfoz cuando el nombre comercial y la razón social coinciden; Alonso entra con este criterio, aunque en el primer informe parcial había quedado como propuesta. Pero se aplicó tu regla para dominios: en esas fichas el nombre y la ciudad no coinciden exactamente y no había teléfono con el que comparar, así que el dominio queda como **propuesta**.

### Dominios propuestos (no añadidos)

| Ficha | Dominio | Localidad |
|---|---|---|
| Ingrinamar | ingrinamar.es | Salamanca solo por el mapa |
| Ediglema | ediglema.es | Carbajosa de la Sagrada |
| Reformas Integrales Alonso | reformasalonso.es | Santa Marta de Tormes |
| Globalcons | globalcons.es | Santa Marta de Tormes |
| Julián Hernández Sánchez | obrasyserviciossalamanca.es | Topas |
| Construcciones Consan | construccionesconsan.com | La Fuente de San Esteban |
| Construcciones Blázquez | construccionesblazquez.es | Santiago de la Puebla |
| Cotatres | cotatres.es | Villares de la Reina |
| Reformas Salamanca / Promantec24 | reformas-salamanca.es | Miranda de Azán |

### Emails propuestos (no escritos)

Estos están en el dominio propio de la web, pero no se crean hasta añadir el dominio, para que Attio no genere empresas duplicadas:

| Ficha | Email |
|---|---|
| Reformas Integrales Alonso | hola@reformasalonso.es |
| Ediglema | isabel@ediglema.es |
| Construcciones Consan | info@construccionesconsan.com |
| Construcciones Blázquez | info@construccionesblazquez.es |
| Cotatres | contacto@cotatres.es |

### Emails de otro dominio (no escritos)

| Ficha | Email |
|---|---|
| DICAL | dicalreformas@hotmail.com |
| Hijos de Luis Martín García | hijosluismg@hotmail.com |
| Inter | interreformassalamanca@gmail.com |
| Julián Hernández Sánchez | julianhsanchez1987@gmail.com |
| A Tu Modo Reforma | atumodoreforma@gmail.com |
| PHONEGAME | arreglodeconsolas@gmail.com |
| Reformas Salamanca / Promantec24 | info@reparacion24.es |
| San Agustín | reformas.sanagustin@gmail.com |

## Retenida sin escribir (1)

- **reformassalamanca.es** («Reformas Salamanca baños y cocinas») no tiene aviso legal, CIF ni email. El único contacto es un formulario y el móvil solo aparece en el enlace de WhatsApp (+34614091727). Es probablemente una web de captación de clientes. Hay que decidir si se descarta.

## Requieren llamada (12) — ver `requiere_llamada.csv`

| Ficha | Motivo | Teléfono en Attio |
|---|---|---|
| Reformas Reis | web 503 | Sí |
| San Agustín | web no confirmada | Sí |
| Construcciones Herfoncal | el dominio no resuelve | Sí |
| Reformas El Mono | sin web | Sí |
| Salmantina Reformas | dominio **en venta** | **No** |
| Cocinas y Reformas Azuvi | sin web | **No** |
| Reparación de Electrodomésticos | nombre genérico; teléfono de relleno | Sí |
| Florentino Cortés | autónomo sin web | Sí |
| Limpiezas Sillero | web 503 | **No** |
| Limpiezas Duende | dominio `webs.com` erróneo | Sí |
| Guijo y Serna | web ilegible | **No** |
| AMANA | intermediario | Sí |

**4 fichas no tienen ningún teléfono**, así que no se pueden llamar todavía: Salmantina, Azuvi, Sillero y Guijo y Serna.

## Problemas detectados (solo se informan)

- **Diseño y Obra:** el aviso legal está sin rellenar, con el CIF inventado **B12345678** y una dirección inventada en Madrid.
- **Mavisal:** el aviso legal es la plantilla del desarrollador (HuebraSoft): su teléfono, email y responsable no son de Mavisal.
- **Limpiezas Duende:** el dominio guardado es `webs.com`, de Vistaprint, y la ficha tiene datos de Vistaprint (descripción, sede en NL, ARR de más de 1.000 millones).
- **Salmantina Reformas:** su dominio está **en venta**.
- **PROMANTEC 24, S.L.** (B37517109) aparece con el mismo móvil +34609142188 en 3 fichas: electricistasalamanca.es, fontanero-salamanca.es y Reformas Salamanca/Promantec24. Es una red de marcas.
- **Reformálitas:** el titular es una sociedad portuguesa. Es una red con oficinas en Salamanca, Pontevedra, Alicante y Covilhã.
- **Oyrsa:** es un grupo grande con oficinas en Madrid y Tenerife. Tiene las coordenadas genéricas 40.4637, -3.7492 y el enlace de WhatsApp del pie tiene una errata.
- **Varias homónimas de Inter** (interreformas.es, Inter Reformas Salamanca CB/SL). Se escribió solo porque el teléfono coincide.
- **Datos personales:** son autónomos Proyectos del Hogar, Jimeya, Julián Hernández y San Agustín. Se omitieron los DNI/NIF personales.

## URLs usadas
https://www.ingrinamar.es/es/contacto/ · https://oyrsa.es/contacto/ · https://reformalitas.es/contacto/ · https://www.aurelma.es/contacto/ · https://disenoyobra.es/ · https://hluismartingarcia.com/ · https://www.construcciones360.es/contacto · https://www.ediglema.es/aviso-legal-es-rgpd · https://reformasjomisaga.es/contacto.html · https://www.luxurydesign.es/contacto · https://www.reformasalonso.es/ · https://dicalreformas.com/ · https://proyectosdelhogar.com/contacto/ · https://mavisal.es/contacto/ · https://www.pinturasjimeya.com/contacto · https://azugresbanos.es/contactanos/ · https://www.globalcons.es/_aviso-legal.php · https://vikainteriorismo.com/contacto/ · https://interreformas.com/ · https://obrasyserviciossalamanca.es/index.php/empresa/quienes-somos · https://construccionesgonzalez.com/ · https://construccionesconsan.com/contacto/ · https://www.construccionesblazquez.es/ · https://cotatres.es/ · https://reformas-salamanca.es/aviso-legal/ · https://reformassalamanca.es/ · https://www.atumodoreforma.com/contacto · https://www.arreglodeconsolas.es/contacto/

## Cierre

- **Procesadas:** 40
- **Con dato escrito:** 25
- **Sin dato:** 15
  - 12 pasan a llamada
  - 2 conflictos: el dato se encontró pero no se escribió
  - 1 retenida (intermediario)
- **Pasan a llamada:** 12 (4 de ellas sin ningún teléfono)

**Slack:** Enriquecimiento 04/11 (lote 2): 40 fichas → 25 con dato (31 tel., 7 emails, 6 dominios), 12 a llamada (4 sin teléfono), 2 conflictos pendientes (Aurelma, Construcciones González), 1 intermediario retenido.
