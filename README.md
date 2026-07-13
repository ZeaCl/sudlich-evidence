# Südlich — Evidencia de Tests E2E

Repositorio de evidencia visual para tests end-to-end de [Südlich](https://github.com/ZeaCl/sudlich).

## Estructura

```
v{version}/
├── suite-report.md          ← resumen de toda la suite para esta versión
├── {test-id}/
│   ├── report.md            ← resumen: fecha, release, resultado, capturas
│   ├── 01-{step}.png        ← screenshot de cada paso
│   ├── 02-{step}.png
│   └── ...
```

## Convenciones

| Regla | Ejemplo |
|---|---|
| Directorio por versión | `v0.1.0/` |
| Directorio por test ID | `f-01a/` |
| Screenshots numerados | `01-landing-page.png` |
| Reporte Markdown por test | `report.md` |
| Capturas contra producción | `sudlich.zea.cl` |

## Script de captura

El script `evidence/f-01a-evidence.cjs` en el repo de [Südlich](https://github.com/ZeaCl/sudlich) genera las capturas automáticamente. Se ejecuta con:

```bash
PLAYWRIGHT_BASE_URL="https://sudlich.zea.cl" node evidence/f-01a-evidence.cjs
```

## Releases

Cada versión de Südlich tiene su directorio de evidencia correspondiente. Si un test no cambió entre versiones, se referencia la evidencia de la versión anterior.
