# Informe de enriquecimiento — 2026-11-04 · Reintento de webs caídas (modo real)

Lista: `supplier_acquisition_pipeline` · Checkpoint: `progress.json` (las 35 fichas llevan el campo `reintento_2026-11-04`) · Llamadas: `requiere_llamada.csv` (61 → 49)

## 1. Entradas duplicadas de PROMANTEC 24

**No se han podido eliminar.** El conector de Attio no tiene ninguna herramienta para borrar entradas de lista. Hay que quitarlas a mano en Attio, desde la lista `supplier_acquisition_pipeline` → *Prospect Discovery*:

| Entry ID |
|---|
| 1fba2ad9-efce-4e7c-ad50-db69245bd4e8 |
| 510c1a87-41fd-4237-ac9f-df25d35e950c |
| 8979791b-190b-43b1-959b-40a302296ab9 |
| bd395a50-1ab2-4563-b528-7f0a25ab31ea |
| c782e317-3224-461e-a1bf-96512ea8cbda |

Hay que conservar la entrada `914e6832-59ad-4883-913e-028edc98a868`, la que está en Outreach y tiene el comentario.

## 2. Reintento de las 35 webs caídas

Se volvieron a probar todas las webs que en los lotes 1 a 6 habían fallado: error SSL, 503, 403, 404, web renderizada con JS o dominio que no resolvía. Se probó https y http, con y sin www, las páginas de contacto y aviso legal, y lectura del HTML con curl.

**Conflictos: 0. Errores: 0.** Antes de escribir se comprobó que cada campo estaba vacío. Después se releyeron las 13 fichas en Attio y todas tienen los valores escritos.

### Enriquecidas (13)

| Ficha | Teléfonos escritos | Persona/email | Dominio | WhatsApp | Fuente |
|---|---|---|---|---|---|
| Pinturas Roma 2009 | +34627218453 | (ya existía) | propuesta | No | https://pinturasroma2009.es/ |
| Disan Pintura & Decoración | +34651118876 | — (gmail) | (ya tenía) | **Sí** | https://www.disandecoracion.com/ |
| Campus PC Informática | — (ya coincidía) | info@campuspc.es | (ya tenía) | widget sin enlace | http://www.campuspc.es/ |
| Impermeabilización y Pintura Moi6 | — (ya coincidía) | info@impermeabilizacionypinturamoi6.es | (ya tenía) | No | http://www.impermeabilizacionypinturamoi6.es/contacto |
| Pinturas Bragado | p2 +34923246389 (p1 ya coincidía) | correo@pinturasbragado.com | (ya tenía) | No | http://pinturasbragado.com/contacto.html |
| SOQUIMSA | +34649965346 | (ya existía) | (ya tenía) | No | http://www.soquimsa.com/aviso-legal |
| Jardinería Monte Nuevo | — (ya coincidía) | info@jardineriamontenuevo.com | (ya tenía) | No | https://jardineriamontenuevo.com/ |
| Persianas Persal | +34923091035 | — | propuesta | No | https://juan5964.wixsite.com/persianaspersal |
| Jardinería La Encina | +34669392761 / +34669392762 (+ comentario con otro móvil y el fijo) | — (infonegocio.com) | propuesta | No | http://www.laencinasalamanca.es/contactar.php |
| Aquaform | +34923157492 / +34923100120 (fijos; no publica móvil) | (ya existía) | propuesta: aquaform.es | No | https://aquaform.es/ |
| Reformas Reis | — (ya coincidía) | — (gmail) | (ya tenía) | No | http://reformasreis.com/1/contactos_838698.html |
| Limpiezas Sillero | +34600036769 / +34923266194 | — (gmail) | **sillerolimpiezas.com** (nombre y ciudad exactos) | **Sí** | https://sillerolimpiezas.com/aviso-legal/ |
| Guijo y Serna | +34648768172 / +34923123122 | (ya existía) | (ya tenía) | **Sí** | https://guijoyserna.es/contacto/ |

**Totales:**
- **Teléfonos añadidos:** 13. No se sobrescribió ninguno.
- **Personas creadas:** 4, todas enlazadas a su empresa. Ninguna creó una empresa nueva por error.
- **Dominios añadidos:** 1.
- **Comentarios:** 1.
- **Fuente y Confianza Alta:** escritas en las 13 fichas.

**Propuestas que no se escribieron:**
- **Dominios:**
  - pinturasroma2009.es: en Carbajosa, con aviso legal de plantilla.
  - persianaspersal.com: en Villares de la Reina; el dominio solo apunta a la web de Wix.
  - laencinasalamanca.es: el nombre no coincide exactamente, porque es «La Encina Servicios Integrados».
  - aquaform.es: la ficha ya tiene aquaformservicios.com.
- **Emails pendientes de que se añada su dominio:** privacidad@persianaspersal.com. Es el email de protección de datos.
- **Emails de otro dominio:** pinturasdisan@gmail.com, pinturamoi6@hotmail.com, reformasisraeljimenez@gmail.com, sillerolimpiezas@gmail.com, laencina_ei@infonegocio.com y javiermurillobenito@gmail.com. Este último es el gmail personal de una persona de SOQUIMSA.

**Para que confirmes:**
- **Aquaform:** la fuente es aquaform.es, mientras que su dominio en Attio es aquaformservicios.com. El aviso legal de aquaform.es es de AQUAFORM INSTALACION Y MANTENIMIENTO SL y publica el mismo email que ya estaba en la ficha (operaciones@aquaformservicios.com), así que es la misma empresa.

### Retenida (1)

| Ficha | Motivo |
|---|---|
| ZARYX Instalaciones | La web carga, pero es una plantilla CM4all genérica, sin titular, CIF ni dirección. El número 923 799 012 encaja con la red de captación 923 79 xx xx. No se escribe nada. |

### Siguen requiriendo llamada (21)

| Ficha | Estado de la web | Teléfono en Attio |
|---|---|---|
| Marviz | Error TLS / 404 | Sí |
| Talleres Eléctricos Lucas | El DNS no resuelve. El negocio está en **Alba de Tormes** | **No** |
| Redes Ópticas Salmantinas | Redirige a **fibritel.com**, un operador de fibra. La vertical está mal | **No** |
| Martín Merchán, Juan Luis | electricom.es no responde. No se confirma que la web sea suya | **No** |
| Construcciones Herfoncal | No es accesible desde aquí. El buscador muestra el móvil 651075326, distinto del de Attio: **posible conflicto** | Sí |
| Limpiezas Duende | No es accesible desde aquí (webs.com) | Sí |
| Electricidad Reyes e Hijos | Página de mantenimiento. El negocio está en Alba de Tormes | **No** |
| PC MEGASTORE | 503 por mantenimiento | Sí |
| KR Informática | El .com es una página vacía de IONOS y el .es ya no existe | Sí |
| Mudanzas Jesús | El dominio ya no existe. La SL figura **inactiva** | Sí |
| Decoraciones J.L. & Chamus | El dominio ya no existe | **No** |
| Comunisal | Redirige a Javier Rivas Real Estate | Sí |
| Tot-Net | Bloqueo de Cloudflare (403) | **No** |
| Vanessa Blanco Casado | El dominio ya no existe | Sí |
| TODO EN CASA | Los dominios .com y .es ya no existen | Sí |
| Kevin Jardinería | Los dos dominios ya no existen | **No** |
| Adm. Fincas María José Navarro | El dominio ya no existe | Sí |
| M.ª Victoria Miguel | **El dominio está comprometido**: sirve spam o una redirección | Sí |
| Carpintería Boni | El dominio ya no existe | **No** |
| PCBox Salamanca | Bloqueo de Cloudflare (403) | Sí |
| Multiservicios H&H | El dominio ya no existe | Sí |

**8 no tienen ningún teléfono:** Talleres Lucas, Redes Ópticas, Martín Merchán, Electricidad Reyes, Chamus, Tot-Net, Kevin y Boni.

## 3. Problemas detectados (solo se informan)

- **mariavictoriamiguel.com está comprometido.** Sirve un script de spam que redirige a una IP externa. Conviene quitar ese dominio de la ficha.
- **Limpiezas Duende** tiene como dominio `webs.com`, y el enriquecimiento automático le ha cargado los datos de Vistaprint: sede en Venlo (Países Bajos), descripción y LinkedIn. Su web real es limpiezasduende.webs.com.
- **Tot-Net** es una empresa nacional con sede en Terrassa y unos 1000 empleados. No es un proveedor local de Salamanca.
- **Redes Ópticas Salmantinas** es un proveedor de fibra (ahora Fibritel). No es un electricista.
- **Fuera de Salamanca capital:** Talleres Eléctricos Lucas y Electricidad Reyes están en Alba de Tormes. En los dos, `primary_city` = Salamanca.
- **Mudanzas Jesús:** su dominio ya no existe y la sociedad figura inactiva desde 2013. Es posible que el negocio haya cerrado.
- **PCBox:** la ubicación de la ficha es la sede central en Reus, no la tienda de Salamanca (ya se informó en el lote 5).
- **Fuera de las verticales de servicios del hogar:** Guijo y Serna (administrador de fincas), Campus PC (informática) y SOQUIMSA (productos químicos para piscinas).
- **Dominios muertos** (ya no existen): kr-informatica.es, mudanzasjesus.es, jlchamuspintores.es, fincasblancocasado.es, todoencasasalamanca.com/.es, kevinjardineria.com, administraciondefincasmariajosenavarro.com, bonicarpinteros.com y obrasyservicioshh.es. Varios siguen como `domains` en Attio.

## 4. "Siguientes fichas"

**No quedan fichas elegibles según la sección 3 de CLAUDE.md.** Todas las fichas en *Prospect Discovery* o *Qualification* que no tenían Fuente y Confianza ya están procesadas (lotes 1 a 6). Opciones para seguir:

1. **Fichas con `fuente` en texto en vez de URL:** fontanero-salamanca.es (ya fusionada), Guillermo López y JMC Clavero. Habría que buscar su URL real.
2. **Limpiar fichas contaminadas con datos de otra empresa:**
   - El Manzano: facebook.com
   - SERVIS: squarespace.com
   - ADMICOCO: ueniweb.com
   - Bella Jardinería: instagram.com
   - Limpiezas Duende: webs.com
   - Toldos Moñita: Coslada
3. **Dominios muertos y comprometidos:** quitarlos de las fichas. Esto requiere tu aprobación, porque implica borrar.
4. **Fase 2 de CLAUDE.md:** tier automático, tareas de llamada para las Tier 1 y borradores de email.

## 5. Resumen global de la jornada (lotes 1 a 6 y reintentos)

| Estado | Fichas |
|---|---|
| Enriquecidas con dato de la web propia | 143 (130 + 13 reintentos) |
| Enriquecidas tras resolver un conflicto con tu aprobación | 4 |
| Requieren llamada | 66 (49 en el CSV; 17 del lote 1 están en su informe) |
| Retenidas o descartadas | 21 |
| Saltada | 1 |
| **Total procesadas** | **235** |

## Cierre de los reintentos

- **Procesadas:** 35
- **Con dato escrito:** 13
- **Sin dato:** 22
  - 21 siguen a llamada
  - 1 retenida por captación
- **Pasan a llamada:** 21 (8 de ellas sin ningún teléfono)

**Slack:** Enriquecimiento 04/11 (reintentos): 35 webs caídas reprobadas → 13 con dato (13 tel., 4 emails, 1 dominio), 21 siguen a llamada (casi todas con dominio ya inexistente), 1 retenida (ZARYX, captación); 0 conflictos, 0 errores. Llamadas pendientes: 66. Las 5 entradas duplicadas de PROMANTEC hay que borrarlas a mano en Attio.
