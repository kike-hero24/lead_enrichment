# Informe de enriquecimiento — 2026-11-04 · Lote 6 (final, modo real)

Lista: `supplier_acquisition_pipeline` · Checkpoint acumulado: `progress.json` (235 fichas) · Llamadas: `requiere_llamada.csv` (61, desde el lote 2)

## 1. Dominios aprobados del lote 5

Añadidos los 8 dominios propuestos, sin errores:
- ayudategruposocial.com
- limpiezasmoran.net
- mueblesjoseangel.com
- carpinteriaestilosalamanca.es
- salamancahomeselect.com
- grupolimcasa.es
- carpinteriaebanisteriacalpe.com
- pinturaydecoracionjoseluis.es

Además se crearon las 2 personas cuyo email solo esperaba a que existiera el dominio: **contacto@salamancahomeselect.com** e **info@grupolimcasa.es**.

## 2. Lote 6: las últimas fichas elegibles

Solo quedaban **15 fichas Tier 3 elegibles** de las 141 Tier 3 que hay. Todas están en Salamanca y en *Prospect Discovery*.

**Conflictos: 0. Errores: 0.**

### Enriquecidas (7)

| Ficha | Teléfonos escritos | Persona/email | Dominio | WhatsApp | Fuente |
|---|---|---|---|---|---|
| AG Cerrajero | — (ya coincidía) | — (hotmail) | — (subdominio de UENI) | **Sí** | https://agcerrajero.ueniweb.com/ |
| Carpintería Hernández (La Encina) | +34686537681 / +34620671449 (+ comentario con el fijo) | — (hotmail) | — | No | https://carpinteriahdez.com/web/contactar/ |
| J.G. Coria Ebanistería | +34699054957 | — (hotmail) | — | No | https://www.carpinteriajgcoria.es/contactar/ |
| Pinturas Hermón 72 | +34667550322 / +34923268851 | — (gmail) | — | No | https://hermon72.blogspot.com/ ⚠️ blog de 2013 (comentario) |
| Limpia tu Casa con Mayte | +34604843908 (+ comentario con los números incoherentes) | contacto@limpiatucasaconmayte.com | limpiatucasaconmayte.com | **Sí** | https://limpiatucasaconmayte.com/contacto/ |
| Smartmovil Salamanca | +34642267634 / +34923051734 | — (gmail) | smartmovilsalamanca.com | **Sí** | https://www.smartmovilsalamanca.com/ |
| Servinarq | +34923176071 | info@servinarq.es | servinarq.es | widget sin enlace | https://servinarq.es/ |

### Retenidas sin escribir (5)

| Ficha | Motivo |
|---|---|
| desatascosdesatrancoslimpiezassalamanca.info | Web de **PROMANTEC 24** (red reparacion24.es) |
| Impermeabilizaciones Salamanca | Web de **PROMANTEC 24**, con el mismo móvil +34609142188 |
| Cerrajero en Salamanca 24 Horas (cerrajero-salamanca.es) | Sin titular, aviso legal ni dirección; dominio genérico |
| La Rana Pintora | Sin aviso legal ni titular y con un número de la **serie 923 79 3x xx** (ver sección 3) |
| GPS Administración de Fincas | No aparece por ningún lado: posible ficha errónea |

### Requieren llamada (3)

| Ficha | Teléfono en Attio | Motivo |
|---|---|---|
| Multiservicios H&H | Sí | La web obrasyservicioshh.es no está accesible |
| Asistencia Técnica Moreno | **No** | Sin web propia |
| Lorenzo Sánchez Muñoz | **No** | Autónomo sin web propia |

## 3. Hallazgos importantes para revisar a mano

**Red PROMANTEC 24, S.L. (B37517109):** el móvil **+34609142188** está ya en **6 fichas**:

| Ficha | Estado |
|---|---|
| electricistasalamanca.es | escrita |
| fontanero-salamanca.es | en Outreach |
| Reformas Salamanca/Promantec24 | escrita |
| Carpintería Salamanca | escrita |
| desatascos…info | retenida |
| Impermeabilizaciones Salamanca | retenida |

Es una sola empresa con muchas marcas o webs. **Recomendación:** consolidarla en una ficha.

**Serie de números 923 79 3x xx, ligada a webs de captación**

| Ficha | Número | Estado / motivo |
|---|---|---|
| Pintura Hogar | 923 793 990 | Descartada: el código de su web reparte los contactos a terceros |
| Empresa de limpieza Salamanca | 923 793 960 | Retenida |
| reformassalamanca.es | 923 793 001 | Descartada |
| La Rana Pintora | 923 793 401 | Retenida |
| fontaneroensalamanca.es | 923 793 496 | **Ya escrita.** El titular está en Madrid |
| Portes y Mudanzas Salamanca | 923 793 190 | **Ya escrita.** Web muy orientada a SEO |

**Recomendación:** revisar en la llamada si **fontaneroensalamanca.es** y **Portes y Mudanzas Salamanca** son los proveedores reales.

**Otros:**
- **Yavoi Europa** (Valencia) es otra red de captación: PowerCharro, ElectroCharro y CharroDesatascos.
- **Mismo móvil en dos fichas:** +34605656166 está en Limpieza Salamanca y en Gestión VUT Salamanca.
- **scraped_rating mayor que 5**, detectado al seleccionar en fichas ya completas: Desatoros Torres (8,8), Saneamientos Cruz (8,7) y Fontaco (8,5).
- **Construcciones Arenas Medina** tiene como dominio `hotmail.es`.
- **Fichas con `fuente` en texto en vez de URL:** fontanero-salamanca.es, Guillermo López y JMC Clavero. Tienen Fuente y Confianza rellenas, así que la regla 3 las excluye.

## 4. Resumen global de la jornada (lotes 1 a 6)

| Estado | Fichas |
|---|---|
| Enriquecidas con dato de la web propia | 130 |
| Enriquecidas tras resolver un conflicto con tu aprobación | 4 (Aurelma, Construcciones González, Toldos Moñita, CUPOSOL) |
| Requieren llamada | 80 (61 en el CSV; las 19 del lote 1 están en su informe) |
| Retenidas o descartadas (captación, fuera de zona, revisar) | 20 |
| Saltada (ya tenía Fuente y Confianza) | 1 |
| **Total procesadas** | **235** |

**No quedan fichas elegibles.** Todas las fichas en *Prospect Discovery* o *Qualification* que no tenían Fuente y Confianza están ya procesadas.

## Cierre del lote 6

- **Procesadas:** 15
- **Con dato escrito:** 7
- **Sin dato:** 8
  - 3 pasan a llamada
  - 5 retenidas
- **Pasan a llamada:** 3 (2 de ellas sin ningún teléfono)

**Slack:** Enriquecimiento 04/11 (lote 6, final): 8 dominios aprobados añadidos; últimas 15 fichas → 7 con dato (9 tel., 2 emails, 3 dominios), 3 a llamada, 5 retenidas. Jornada completa: 235 fichas procesadas, 134 con dato, 80 a llamada; no quedan fichas elegibles. Ojo a las redes de captación (PROMANTEC 24, Yavoi, serie 923 79 3x).
