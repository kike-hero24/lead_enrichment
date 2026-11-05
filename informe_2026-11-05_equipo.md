# Informe de enriquecimiento: 2026-11-05, limpieza y equipo de agentes (modo real)

Lista: `supplier_acquisition_pipeline` (669 entradas) · Checkpoint: `progress.json` (lote `equipo_2026-11-05`) · Llamadas: `requiere_llamada.csv` (107 filas)

## 1. Avance de la tarea

Antes de empezar se hizo un censo completo de las 669 entradas de la lista.

| Indicador | Antes (04/11, tras los lotes 1 a 6) | Ahora | % |
|---|---|---|---|
| Entradas revisadas por el proceso | 236 | 553 | 83 % |
| Entradas que no necesitan revisión (ya tenían teléfono y persona) | — | 102 | 15 % |
| **Cobertura total (revisadas o completas)** | — | **655 / 669** | **98 %** |
| Con teléfono | 352 | **541** | 81 % |
| Con persona/email | 367 | **399** | 60 % |
| Con teléfono y persona | ~202 | **364** | 54 % |

**Las 14 entradas restantes quedan fuera del alcance de CLAUDE.md:**
- 7 no son proveedores: gmaim.com, Mawrble, Spanish Consulate, iCloud, Valtria, RealNames y una ficha sin nombre (reformasalamanca.es). Recomendación: quitarlas de la lista.
- 6 están en Outreach o Prioritization, etapas que no se procesan: Instalaciones Espinosa, Cyssa, Fontanería Sin Obra FSD, Fontanería Iván Mesa, Fonclisa y By transport.
- 1 es la entrada duplicada de Bella Jardinería (fcee7dde). La otra entrada ya se procesó.

**En la práctica, el 100 % de los leads dentro del alcance ya está revisado.** Lo que falta para completar las fichas está en manos del equipo: las llamadas y las decisiones pendientes de la sección 5.

## 2. Limpieza de fichas contaminadas

**A. 17 empresas tenían como dominio una plataforma o un directorio.** El enriquecimiento automático de Attio les había cargado los datos de esa plataforma (ubicación, descripción, LinkedIn, Twitter, Facebook, categorías, plantilla de empleados, facturación...). Se quitó el dominio erróneo y se borraron esos campos.

| Ficha | Dominio antes | Dominio ahora |
|---|---|---|
| Jardines y Diseños Francisco Montiel | beedigital.es | xn--jardinesydiseofranciscomontiel-q4c.com |
| Splash Pools Mijas | electronbox.net | splashpoolsmijas.com |
| Comercial Rogelio | clima.com | comercialrogelio.com |
| Damaz Multiservicios | yahoo.com | damaz.es |
| Construcciones Arenas Medina | hotmail.es | construccionesarenasmedina.es |
| Regna Tec | proveedores.com | (vacío) |
| AyG Cerrajeros | profesionales-malaga.com | (vacío) |
| Cerrajería Crifer | qdq.com | (vacío) |
| Adfincosol | cronoshare.com | (vacío) |
| Britannia Southern | thinkspain.com | (vacío; luego southern.es, ver abajo) |
| ADMICOCO | ueniweb.com | (vacío) |
| Construcciones Miguel Ruz | elsoldeantequera.com | (vacío) |
| Limpiezas Duende | webs.com | (vacío) |
| Jardinería El Manzano | facebook.com | (vacío) |
| Bella Jardinería | instagram.com | (vacío) |
| SERVIS Salamanca | squarespace.com | (vacío) |
| Electrónica 2000 | provenexpert.com | (vacío) |

**Campos que no se pudieron borrar**, porque son de solo lectura en Attio:
- `logo_url`, en 16 fichas.
- `twitter_follower_count`, en 12 fichas.
- Las interacciones de Damaz, que vienen de emails reales con su antigua dirección de yahoo.com.

**B. 28 teléfonos sin el prefijo +34**, por ejemplo `+952582950`: se corrigieron a `+34XXXXXXXXX`.
- No se pudo corregir el `+68638785` de Regna Tec, que tiene 8 dígitos.
- Los números extranjeros (+44, +45, +33) son válidos y no se tocaron.

## 3. Enriquecimiento de los 319 leads pendientes

Eran fichas en Prospect Discovery a las que les faltaba teléfono o persona con email. En los lotes anteriores se habían saltado porque ya tenían Fuente y Confianza (regla 3), casi siempre con un directorio como fuente (aeslux, Google Maps...).

**Cómo se organizó el equipo:**
- **Investigación:** 12 agentes en solo lectura, uno por tanda de 22 a 27 fichas, ordenadas por prioridad de vertical y tier. Solo usaron datos publicados en la web propia de cada negocio.
- **Decisión:** un script aplicó las reglas de CLAUDE.md a los resultados y revisé a mano los casos dudosos.
- **Escritura:** 12 agentes de escritura. Antes de escribir cada campo comprobaron que estaba vacío y después releyeron las fichas.

**Criterio aplicado** en las fichas que ya tenían Fuente y Confianza:
- Solo se rellenan campos vacíos.
- **La `fuente` previa no se sobrescribe.** En su lugar se deja un comentario en la entrada con la URL de la web propia y la fecha.
- Solo se escribió `fuente` y `confianza` Alta donde estaban vacías (4 fichas).

### Resultado

| Estado | Fichas |
|---|---|
| Enriquecidas | **212** |
| Verificadas: la web coincide con lo que ya había | 6 |
| Requieren llamada | 58 |
| Retenidas (captación, fuera de zona o no proveedor) | 41 |
| Conflicto (sin escribir) | 2 |
| **Total** | **319** |

**Datos escritos:**
- **Teléfonos:** 280. No se sobrescribió ninguno.
- **Personas con email creadas:** 32. Todas están en el dominio de su empresa y ninguna creó una empresa nueva por error.
- **Dominios añadidos:** 1 (southern.es en Britannia Southern, porque el teléfono coincide).
- **Fuente y Confianza Alta:** en 4 fichas (MacWinRepair, Aquanur, Casa de las Persianas y Prodistele).
- **Comentarios con la fuente o con teléfonos extra:** 208.

**Errores de escritura: 0.** La ejecución se cortó a mitad por el límite de uso; al reanudarla, los agentes comprobaron cada campo y comentario antes de escribir, así que no se duplicó nada.

Hay **88 fichas** cuya web tiene enlace o botón de WhatsApp. Está anotado en `progress.json` y no se escribió en Attio.

### Conflictos (no se escribió nada)

| Ficha | Motivo |
|---|---|
| Britannia Southern, segunda entrada (5ea0f5c9) | Los teléfonos de Attio (+34631269407 y +4593942898) no aparecen en la web propia, que publica +34952470707 |
| Cerrajería Daniel Martínez | La propia web se contradice: el aviso legal y la página de contacto dan teléfono, email y dirección distintos |

### Retenidas (41)

**Webs de captación (keyword, sin titular, agencias SEO o redes multiciudad):**
- Reparar Tu Casa / Soluciones González: red de urgencias 24 h en varias ciudades, con una dirección falsa en California.
- Técnicos Bermeja
- Reformantia
- Casabermeja (construccionesyreformasmalaga.es)
- Irureform
- VKM Reformas
- Reformas Integrales Málaga
- Multiservicios Antequera
- Reforvis
- Desatoros Delimsa
- Técnico Electrodomésticos Fuengirola
- Alpaca Limpiezas: 5 sedes con números correlativos 951 20 4x xx.
- Multiservicios Málaga: el aviso legal es una plantilla sin rellenar.
- Cerrajeros Salamanca (webnode)
- Cerrajero Cerca
- Cerrajeros La Universidad 24h
- Carpinteros Salamanca: su aviso legal dice que es un portal de captación.
- Desatascos Andrés
- Desatascos Ciudad de Salamanca
- Cerrajero Antequera
- Servicio Técnico Fagor Málaga
- carpinteromalaga.com
- Control de Plagas Fuengirola
- Archimede Málaga
- AyG Cerrajeros: 3 entradas, en profesionales-malaga.com.

**Fuera de zona:**
- Construcciones Arenas Medina (Otura, Granada)
- DMR Control de Plagas (Motril)
- Hisan (Écija)
- Limpiezas Comodín (Barcelona)
- Cerrajeros Vélez-Málaga (titular en Granada)

**No son proveedores locales:**
- GuestReady: plataforma internacional.
- ALS Aquimisa: laboratorio del grupo ALS, con ubicación en Australia.
- Decomorado: solo aparece en un portal de empresas.
- Construcción y Reformas Azuaga: su dominio es ahora un directorio.
- Regna Tec: 5 entradas; solo aparece en directorios y regna-tec.com no responde.

### Requieren llamada (58), ver `requiere_llamada.csv`

Los motivos son:
- No tienen web propia, sobre todo electricistas autónomos de Salamanca listados en AESLUX.
- Su web está caída o ya no existe: montajeselectricoslaser.com, electrobytesl.com, arlux.es, ravenergia.es, deccoandy.com, mifincaes.com, iclean-spain.com, gardenviverossanchez.com, cerrajeriaypuertas2010.com, entre otras.
- Su web no publica teléfono: Govera y Valora Construcción.

## 4. Propuestas que no se escribieron

**Emails de un dominio que la ficha no tiene (28).** La ficha no tiene dominio y el teléfono no permitía confirmar que la web es de la misma empresa. Si apruebas añadir el dominio, se crean las personas:
- Lectriciti, Asprel, Tecinsa, Ingeniería Sierra Técnicos, Farcav, T. Crespo, Solórzano (somelec.es), Construcciones Eléctricas Jara (trafojara.com), TID Eléctricos, Enersir y Boyero de San José (proyectosdelhogar.com).
- Electronova, Electro Helmántica, Helmanred, Meins, Coforsa, Desatascos Isma, GerHogar, Aplicaciones Bioquímicas, Reparaciones Guerrero, El Llavín, Home & Harmony, Electrónica 2000, Update Informática (updatesi.com), Reformas Integrales (.pro), Fluinsa, Klimacentro (me.com) y LMM (limsama.com).

**Dominios que habría que corregir.** El dominio de Attio no funciona o es de otro negocio, y la web real es otra:

| Ficha | Dominio en Attio | Web real |
|---|---|---|
| Semateq | semateq.net | semateq.es |
| MB Reformas | mbreformashogar.com | reformasmb1.com |
| Gálvez & Sánchez | galvezysanchez.com | administracionesgalvezysanchez.com |
| LEFEMA | lefema.es | limpiezalefema.es |
| Pintor Alhaurín | pintormalaga.com | pintoralhaurindelatorre.com |
| Mudanzas La Seda | mudanzaslaseda.com (web de Murcia) | mudanzasmalaga-laseda.es |
| Ebanistería Marcos Benito | ebanisteriamarcosbenito.es | ebanisteriamarcosbenito.com |
| Cerrajería Luengo | cerrajeria-luengo.com | cerrajerialuengo.es |
| Cerrajería Daniel Martínez | danielmartinez.es | cerrajeriadanielmartinez.com |
| DMR | dmr.pm | controldeplagasmalaga.es |

Sin dominio todavía: MASAT (calefaccionsalamanca.com), Tobío (climatobio.es) y Climaterm (climatermsalamanca.com).

## 5. Problemas detectados (solo se informan)

- **Entradas duplicadas en la lista:**
  - Las 5 de PROMANTEC 24 siguen pendientes de borrar a mano: 1fba2ad9, 510c1a87, 8979791b, bd395a50 y c782e317.
  - Regna Tec tiene 5 entradas.
  - Britannia Southern tiene 2.
  - AyG Cerrajeros tiene 3.
  - Mudanzas La Seda tiene 2 (6ec60f2a y e92d1d08).
  - Bella Jardinería tiene 2.
- **Ubicación incorrecta que no viene de una plataforma** (no se ha tocado):
  - Toldos Moñita: Coslada.
  - PCBox: Reus.
  - Mudanzas Cárdenas: Madrid.
  - CESFAM: San Francisco.
  - SATALI: Valencia.
  - Jardines Montiel y Arenas Medina: coordenadas genéricas.
- **Britannia Southern:** al añadir southern.es, Attio rellenó solos el logo y las categorías. Conviene revisarlos.
- **Teléfonos dudosos:**
  - Claudino: el móvil +34649250000 parece falso; no se escribió. Su comentario repite por error el fijo, que ya está en `phone_number`.
  - Pintores Burrueco: publica dos números consecutivos (627501348 y 627501349).
  - Carpintería Mácar: un número parece una errata del otro; está anotado en un comentario.
  - Informático Alhaurín: la página de contacto y el aviso legal dan móviles distintos.
- **Fuera de las verticales de servicios del hogar:** Mars Administradores, Guijo y Serna, Gálvez & Sánchez y Adfincosol (administración de fincas), Easy Rent e IVI Real Estate (inmobiliarias) y Laboratorio SersaLab.
- **Fuentes que siguen apuntando a un directorio:** Regna Tec, Crifer, Adfincosol, Miguel Ruz, Electrónica 2000, AyG y ADMICOCO (esta última con confianza Alta sobre ueniweb).
- **Ratings mayores que 5:** 6 fichas, con valores de 7,7 a 8,7. Parecen estar en escala de 10.

## Cierre

- **Procesadas:** 319
- **Con dato escrito:** 212
- **Sin dato:** 107
  - 58 a llamada
  - 41 retenidas
  - 6 verificadas sin cambios
  - 2 en conflicto
- **Pasan a llamada:** 58
- **Limpieza:** 17 fichas contaminadas y 28 teléfonos sin prefijo

**Slack:** Enriquecimiento 05/11 (equipo de agentes): limpiadas 17 fichas contaminadas (dominios de plataformas y sus datos) y 28 teléfonos sin +34. Revisados los 319 leads que faltaban → 212 con dato (280 tel., 32 emails), 58 a llamada, 41 retenidas (captación/fuera de zona), 2 conflictos; 0 errores. Lista: 98 % revisada; 81 % con teléfono (antes 53 %).
