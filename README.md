# Mirage Panel — Documentación

Sitio de documentación (Mintlify) con las guías del panel de administración de **Mirage World**.

Contenido en **español (LATAM)** para operadores del panel.

## Requisitos

- Node.js 18+
- Cuenta Mintlify (para deploy en producción)

## Desarrollo local

```bash
cd mirage-panel-docs
npx mintlify dev
```

Abre la URL que imprime la CLI (por defecto `http://localhost:3000`).

Validar configuración:

```bash
npx mintlify validate
```

## Estructura

```
mirage-panel-docs/
├── docs.json                 # Config Mintlify v4
├── index.mdx                 # Landing / índice
├── general/                  # Guías GENERAL
├── configuracion/            # Guías CONFIGURACIÓN
├── images/
│   ├── spots/                # Capturas Spots (locales)
│   └── shops/                # Capturas Tiendas (locales)
└── README.md
```

Las capturas de las guías 01–13 usan URLs del CDN de Sanity. Spots y Tiendas usan PNG locales en `images/`.

## Deploy en Mintlify

1. Subí este repo a GitHub.
2. En [Mintlify Dashboard](https://dashboard.mintlify.com) conectá el repositorio.
3. Indicá la raíz del repo (donde está `docs.json`).
4. Mintlify despliega en cada push a la rama configurada.

No hace falta secretos en este scaffold para preview local.

## Navegación

- **GENERAL:** Resumen, Growth, Jugadores, Cuentas, Personajes, Herramientas GM, Base de datos
- **CONFIGURACIÓN:** Tiendas, Spots, Mpoints, Rental items, Event Items, Eventos, Cash Shop, Monstruos
