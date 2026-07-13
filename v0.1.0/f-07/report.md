# F-07 — Estado vacío (0 fondos)

- **Release**: v0.1.0
- **Fecha**: 2026-07-13
- **Entorno**: Producción (`https://sudlich.zea.cl`)
- **Resultado**: ✅ PASS

## Descripción

Verifica que cuando la API de fondos devuelve una lista vacía, el microfrontend muestra el mensaje `"No hay fondos creados todavía."` en vez de una tabla vacía o un error.

## Técnica

Se usa **route interception** de Playwright para mockear las respuestas de `funds.zea.cl` y `cerebelum.zea.cl` con datos vacíos, sin necesidad de crear una organización sin fondos.

```js
await page.route('https://funds.zea.cl/funds', async (route) => {
  await route.fulfill({ body: JSON.stringify({ items: [], total: 0 }) })
})
```

## Capturas

| Paso | Archivo | Descripción |
|---|---|---|
| 1 | `01-logged-in.png` | Usuario logueado en CraniumShell |
| 2 | `02-empty-message.png` | Página de fondos con mensaje "No hay fondos creados todavía." |

## Verificaciones

- [x] Mensaje "No hay fondos creados todavía." visible
- [x] Tabla `<table>` NO visible (no hay datos que mostrar)
- [x] Mock de API funciona correctamente (route interception)
