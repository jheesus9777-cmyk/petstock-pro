# PetStock Pro v68

Sistema de inventario, ventas y finanzas para tienda de mascotas.  
Aplicación **single-file** (React 18 + Recharts + Tailwind) que funciona 100% en el navegador con `localStorage`.

## Características

- **Productos**: Stock, cobertura (DOC), semáforos, reorden automático
- **Ventas Hoy**: Registro rápido, deshacer, cierre de día → historial
- **Herramientas**: Buscador, wizard, import/export + suite de Tests
- **Finanzas ($$$)**: Rentabilidad, pronóstico 20 días (S1-S4), proveedores y pedidos consolidados
- Bottom dock estilo app nativa
- Persistencia local completa (`petstock:*` keys)

## Cómo usar

1. Abre `index.html` en cualquier navegador moderno (Chrome / Edge / Safari / Firefox).
2. O súbelo a GitHub Pages / Netlify / Vercel como sitio estático.
3. Los datos se guardan en el navegador (localStorage). Haz backup desde Herramientas.

## Estructura de datos (localStorage)

| Clave | Contenido |
|-------|-----------|
| `petstock:productos:v1` | Array de productos |
| `petstock:historial:v1` | Objeto `{ productoId: [cantidades...] }` |
| `petstock:ventasHoy:v1` | Ventas del día actual |
| `petstock:bundle:v1` | Snapshot de seguridad (productos + historial) |
| `petstock:lastTab` | Última pestaña abierta |

## Versión

**v68** — FIX ROOT + Parches A-I completos

Mejoras de rendimiento aplicadas:
- Eliminación de `setInterval` agresivos
- Glass blur desactivado en móvil
- Badge del dock solo por eventos
- Observer ligero en lugar de polling constante
- CSS consolidado (menos reglas duplicadas)

## Licencia

Uso privado / interno de tienda.  
Hecho con ❤️ para gestión real de stock de mascotas.
