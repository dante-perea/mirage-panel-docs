# Guías del panel JugarMU

Documentación en español del panel de jugarmu.com. La navegación se define en `docs.json` y sigue las secciones actuales del producto.

## Desarrollo

Usar la CLI oficial de Mintlify (`mint`):

```sh
npx mint dev --no-open
npx mint validate
npx mint broken-links
```

Referencia: https://www.mintlify.com/docs/es/cli/install

## Mantenimiento

Antes de documentar un control, comprobar la instancia, la versión y la pantalla autenticada. Distinguir el estado mostrado de la ejecución real de una operación. No asumir confirmaciones: varios botones envían cambios directamente.

Las nuevas capturas están en `images/actual/`. No incluir credenciales, correos de jugadores ni datos privados. Las guías de funciones específicas deben indicar su disponibilidad por instancia.

`audit/` conserva los manifiestos de revisión. `SCREENSHOT-GAPS.md` identifica la evidencia que todavía falta; una compilación correcta no equivale a una auditoría completa. Las evidencias de sesión se mantienen locales.

Mintlify publica desde la rama configurada en su integración con GitHub. Antes de dar una entrega por terminada, comprobar el sitio publicado y el contenido recuperado por su MCP.
