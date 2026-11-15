# 9. Uso de GitHub

**URL del repositorio:** https://github.com/matcontardo/ihc-u2-reportaya

Usamos GitHub para guardar las versiones del trabajo, dejar registro de los acuerdos del equipo y publicar el prototipo con GitHub Pages.

## 9.1 Organización del repositorio

| Carpeta / archivo | Contenido |
|---|---|
| `README.md` | Presentación del proyecto, integrantes, cómo ver el prototipo y estructura del repo. |
| `RESUMEN.md` | Archivo resumen de la entrega (una página). |
| `docs/` | Un archivo por apartado del informe (01 a 09), acuerdos del equipo y bitácora. |
| `diagramas/` | Modelo conceptual, mapa de contenidos y flujo de usuario (fuente `.dot` de Graphviz + imagen `.png`). |
| `prototipo/baja-fidelidad/` | Bocetos de las alternativas A, B y C. |
| `prototipo/media-fidelidad/` | Prototipo navegable (`index.html`) y carpeta `capturas/`. |
| `informe/` | Informe final en Word. |

## 9.2 Registro del proceso

- **Commits por etapa:** cada commit corresponde a un avance del proceso de diseño (requisitos, alternativas, modelo conceptual, prototipo, etc.), con mensajes descriptivos en español.
- **Issues:** cada apartado del trabajo se registró como un *issue* con su responsable y se cerró al completarlo. Así se puede seguir qué se hizo y cuándo.
- **Acuerdos del equipo:** el archivo `docs/acuerdos-equipo.md` contiene los roles, las reglas para trabajar en el repo y las decisiones de diseño importantes.
- **Bitácora:** `docs/bitacora.md` registra los avances y las decisiones tomadas.
- **Versiones del prototipo:** el boceto (v1) y el prototipo navegable (v2) quedan en carpetas distintas para mostrar la evolución de la fidelidad.
- **Release:** la versión entregada se marca con la etiqueta `v1.0-entrega-u2`.
