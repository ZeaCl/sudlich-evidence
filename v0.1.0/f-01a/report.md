# F-01a — Sidebar click Fondos → iframe carga

- **Release**: v0.1.0
- **Fecha**: 2026-07-13
- **Entorno**: Producción (`https://sudlich.zea.cl`)
- **Resultado**: ✅ PASS

## Descripción

Verifica que al hacer click en "Fondos" en el sidebar de CraniumShell, el sistema navega a `/pieces/funds`, carga el microfrontend en un iframe, y la tabla de fondos se renderiza correctamente.

## Capturas

| Paso | Archivo | Descripción |
|---|---|---|
| 1 | `01-landing-page.png` | Página de login con branding Südlich |
| 2 | `02-shell-loaded.png` | CraniumShell cargado post-login, sidebar visible |
| 3 | `03-fondos-highlighted.png` | MANAGEMENT expandido, link "Fondos" resaltado |
| 4 | `04-funds-page-loaded.png` | Navegación a `/pieces/funds` completada |
| 5 | `05-funds-table-loaded.png` | Iframe con tabla de fondos (4 filas) cargada |

## Verificaciones

- [x] Login OAuth2 → CraniumShell cargado
- [x] Sección MANAGEMENT visible y expandida
- [x] Click en "Fondos" navega a `/pieces/funds`
- [x] Iframe del microfrontend carga
- [x] `<h1>Fondos</h1>` visible dentro del iframe
- [x] `<table>` visible con `tbody tr` (4 fondos)
