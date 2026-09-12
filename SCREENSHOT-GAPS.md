# Screenshot gaps — capturas que faltan

Flujos que todavía necesitan **capturas nuevas** (diálogos, confirmaciones o pestañas sin shot dedicado). Bro puede capturarlas en la próxima pasada.

## Diálogos / confirmaciones (alta prioridad)

| Flujo | Página(s) doc | Qué capturar |
|-------|---------------|--------------|
| **Expulsar** — diálogo de confirmación | `general/jugadores/expulsar` | Modal tras pulsar **Expulsar** (texto + Cancelar/Confirmar). Ya tenemos la tabla con el botón. |
| **Banear** — confirmación (listado y/o perfil) | `general/cuentas/restablecer-banear` | Modal tras **Banear** / **Banear cuenta**. |
| **Restablecer** / **Restablecer contraseña** — resultado o confirmación | `general/cuentas/restablecer-banear` | Modal o toast tras restablecer (si muestra contraseña temporal / aviso). |
| **Teletransportar** — confirmación | `general/personajes/teletransportar` | Modal/toast tras **Teletransportar** (si existe). Botón ya está en `images/gaps/personajes-teleport.png`. |
| **Curar / restaurar** — feedback | `general/personajes/curar-resetear` | Toast/resultado tras curar (si existe). |
| **Resetear personaje** — confirmación destructiva | `general/personajes/curar-resetear` | Modal de confirmación antes de resetear. |
| **Detener** servicio — confirmación | `general/resumen/detener-servicio` | Modal tras **Detener** en Resumen → Servidores. |
| **EMPEZAR evento** — confirmación / estado en curso | `configuracion/eventos/disparar-manual` | Modal o cambio de UI tras disparo (sin disparar en prod si no hace falta; lab OK). |
| **Rentar** — confirmación / ítem en grilla | `configuracion/rental-items/rentar-objeto` | Resultado tras **Rentar** (ítem aparece en inventario). |
| **Vaciar / Fijar** Mpoints — confirmación | `configuracion/mpoints/sumar-fijar-vaciar` | Modal o saldo actualizado tras Fijar/Vaciar. |
| **Guardar** Cash Shop listing — listing nuevo en lista | `configuracion/cash-shop/crear-listing` | Listings tras Guardar (antes/después). |
| **Quitar** Event Items — confirmación | `configuracion/event-items/anadir-quitar` | Si hay modal al quitar. |
| **Añadir zona** Spots — zona nueva en lista/preview | `configuracion/zonas/anadir-zona` | Antes/después de **Añadir zona**. |
| **Eliminar** zona — confirmación | `configuracion/zonas/eliminar-zona` | Si hay modal. |

## Pestañas / vistas sin captura dedicada

| Área | Qué falta |
|------|-----------|
| Growth | Pestañas **Activation**, **Retention**, **Revenue**, **Referral** (solo tenemos Awareness + Acquisition). |
| Herramientas GM | Pestañas **Eventos**, **Plugins**, **Consola** (solo Anuncios + Ajustes del juego). |
| Eventos | Pestañas **Lost Treasure** y **Todos contra todos**. |
| Login | `images/panel/login.png` es duplicado de Resumen en coverage; hace falta un shot real de login si se documenta el acceso. |
| Sidebar | `images/panel/sidebar.png` también duplicado; opcional crop limpio del menú. |

## Ya cubierto recientemente (gaps/)

No re-capturar salvo que quieran mejor crop:

- `jugadores-mensaje-dialog.png` — diálogo Mensaje
- `cuentas-boveda-add.png` — diálogo Añadir objeto (bóveda)
- `gm-anuncio-form.png` — formulario Anuncios
- `rental-form.png` — formulario Rental
- `personajes-teleport.png` / `personajes-curar.png` / `personajes-reset.png` — acciones Personajes
- `cash-shop-crear-form.png` — formulario Crear listing
- `monstruos-editor-focus.png` — editor Monstruos
- `eventos-page.png` — Invasiones + EMPEZAR visible

## Notas

- Preferir UI en español LATAM, sin datos sensibles (correos reales OK si ya están en panel demo).
- No hace falta incluir badge de estado ni pie de CPU/RAM en el crop si se puede evitar ruido.
- Guardar nuevos archivos bajo `images/gaps/` o `images/panel/` y enlazar desde el MDX correspondiente.
