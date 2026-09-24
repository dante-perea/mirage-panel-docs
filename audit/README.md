# Renovación completa de las guías

Estado: en curso. No es una auditoría terminada ni publicada.

Fuente del panel: `dante-perea/openmu-host`, main `beb3308`. Base de documentación: `87b71e1`.

`panel-coverage.json` conserva el inventario de todas las páginas anteriores y los recorridos del nuevo panel. Ningún recorrido está marcado como verificado antes de visitar la interfaz autenticada.

## Criterios de entrega

- Revisar cada sección, pestaña, editor y confirmación sin ejecutar cambios destructivos sobre jugadores reales.
- Capturas nuevas de la interfaz real, sin credenciales ni datos personales.
- Guías en español con ruta exacta, pasos, efecto, confirmación de guardado y límites de cada versión.
- Reemplazar todas las guías antiguas o redirigirlas a su sustituto; no dejar páginas desactualizadas en la búsqueda MCP.
- Validar navegación, enlaces, imágenes y compilación antes de publicar.
- Consultar la documentación publicada desde el MCP de Hermes y repetir la pregunta sobre el set +9.

## Hallazgo confirmado en el código del panel

`Ajustes del juego → Plugins` incluye `Set de bienvenida`, dentro de `Bienvenida y progresión`. El interruptor permite desactivar las nuevas entregas y guarda automáticamente; no retira los objetos ya entregados.

El texto del plugin menciona configuración de duración/nivel/Excellent/arma, pero este componente solo presenta un botón Configurar para destinos expresamente implementados. No documentar un editor del set sin verlo realmente.

## Acceso y evidencia actual

El usuario inició sesión. Se visitó el panel de `openmublue` el 24 de septiembre de 2026 y se capturaron Inicio, Experiencia, Objetos y Zen, Resets, Combate y chat, Set de bienvenida, Jugadores y Personajes (filtrado a una cuenta de prueba).

No se modificaron ajustes ni datos de jugadores. La auditoría completa sigue pendiente. Esta instancia oculta del menú las funciones exclusivas de servidores personalizados.

La búsqueda de Set de bienvenida devuelve dos filas con el mismo título. Para detener nuevas entregas hay que identificar `Add 48h starter rental set and weapon` en Detalles; la otra es una migración histórica.

## Continuación: cobertura ampliada

Fuente actual contrastada: `fab146b` (main consultado el 24 de septiembre). Se reescribieron 35 guías de inicio/configuración/GM y 32 de jugadores/tiendas/premios/ayuda/plugins, además de las 18 fichas de plugins y los borradores iniciales de ajustes y bienvenida. Los manifiestos individuales indican los archivos y la evidencia; estos conteos no prueban que toda la auditoría esté terminada.

Se retiraron seis páginas de Growth: no existe ese conjunto de pantallas en las rutas y componentes actuales. `retired-pages.json` conserva el motivo y las rutas antiguas se redirigen a Actividad. La navegación nueva sigue los nombres del panel. El análisis local de enlaces revisó 104 MDX y no encontró referencias Markdown internas ni páginas de navegación faltantes.

### Pendientes concretos

- Trece guías antiguas de funciones personalizadas (Monedas, Tienda premium, Alquileres e Invasiones) siguen sin revisión visual completa. No publicar este estado como renovación completa.
- La cuenta autenticada no accede a `ecxon`; tampoco por la ruta de operador. Se solicitó al usuario una instancia accesible con esas funciones.
- La pantalla de jugadores artificiales de `openmublue` devuelve un error de lectura (referencia 2184287713). Falta una interfaz operativa para la captura y revisión.
- Falta guía y captura segura de Mi cuenta, validación de todos los encuadres, prueba renderizada del sitio, publicación y validación MCP/Hermes.
- No hubo jugadores conectados para capturar los botones Mensaje/Expulsar en una fila real. Su comportamiento se contrastó con `PlayersScreen.tsx`; las guías explican que la captura tiene cero sesiones.
- No se ejecutaron cambios de contraseñas, bloqueo, resets, teletransporte, curación ni escrituras de inventarios durante esta revisión.
- `npx --no-install mintlify validate` no arrancó por paquete ausente. La validación con `npx --yes mint@latest validate` finalizó con código 0 y `success build validation passed`. Esto verifica compilación local, no publicación ni exactitud de las guías pendientes.

Las trece guías personalizadas ya se reescribieron contra el código actual y se añadió VIP; ver custom-source-review.json. Todavía no tienen captura ni verificación visual de instancia compatible. No equivale a completar esa cobertura.
