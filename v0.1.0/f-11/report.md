# F-11 — Click real "+ Crear Fondo" → wizard

- **Release**: v0.1.0
- **Fecha**: 2026-07-13
- **Entorno**: Producción (`https://sudlich.zea.cl`)
- **Resultado**: ✅ PASS

## Descripción

Verifica que al hacer click real en el botón "+ Crear Fondo" desde la página de fondos, el sistema navega al wizard de creación y muestra el paso 1 (Identidad) con sus campos.

**Navegación vía sidebar** (flujo real): click en MANAGEMENT → Fondos → iframe → click "+ Crear Fondo" dentro del iframe → wizard carga.

## Capturas

| Paso | Archivo | Descripción |
|---|---|---|
| 1 | `01-sidebar-fondos-highlighted.png` | Sidebar con MANAGEMENT expandido, "Fondos" resaltado |
| 2 | `02-funds-page-with-sidebar.png` | UI completa: sidebar + tabla de fondos en sección central |
| 3 | `03-create-btn-in-iframe.png` | Botón "+ Crear Fondo" resaltado dentro del iframe |
| 4 | `04-wizard-with-sidebar.png` | UI completa: sidebar + wizard paso 1 "Identidad" cargado |

## Verificaciones

- [x] Botón "+ Crear Fondo" visible y clickeable
- [x] Navegación a `/mf/create-fund.html`
- [x] `<h1>Crear Fondo</h1>` visible
- [x] Stepper muestra los 4 pasos: Identidad, Parámetros Financieros, Ciclo de Vida, Revisión
