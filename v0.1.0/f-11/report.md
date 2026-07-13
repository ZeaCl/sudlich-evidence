# F-11 — Click real "+ Crear Fondo" → wizard

- **Release**: v0.1.0
- **Fecha**: 2026-07-13
- **Entorno**: Producción (`https://sudlich.zea.cl`)
- **Resultado**: ✅ PASS

## Descripción

Verifica que al hacer click real en el botón "+ Crear Fondo" desde la página de fondos, el sistema navega al wizard de creación y muestra el paso 1 (Identidad) con sus campos.

A diferencia de F-05 que solo verificaba el atributo `href`, este test hace **click real** y verifica que la navegación ocurre y el wizard carga.

## Capturas

| Paso | Archivo | Descripción |
|---|---|---|
| 1 | `01-funds-table.png` | Página de fondos con tabla de 4 fondos |
| 2 | `02-create-btn-highlighted.png` | Botón "+ Crear Fondo" resaltado antes del click |
| 3 | `03-wizard-step1.png` | Wizard cargado: paso 1 "Identidad" con formulario |

## Verificaciones

- [x] Botón "+ Crear Fondo" visible y clickeable
- [x] Navegación a `/mf/create-fund.html`
- [x] `<h1>Crear Fondo</h1>` visible
- [x] Stepper muestra los 4 pasos: Identidad, Parámetros Financieros, Ciclo de Vida, Revisión
