# Acuerdos del equipo

## Integrantes y roles

| Integrante | Rol principal |
|---|---|
| Matías Contardo | Coordinación, contexto de la planta (requisitos), repositorio GitHub y prototipo navegable |
| [Integrante 2] | Alternativas, modelo conceptual y metáfora |
| [Integrante 3] | Arquitectura de información, flujo de usuario y diseño visual/emocional |

> Todos revisamos el informe completo antes de la entrega.

## Reglas de trabajo en el repositorio

1. Escribimos los mensajes de commit en español y en presente, indicando el apartado. Ejemplo: `docs: agrega tabla de requisitos (apartado 1)`.
2. Prefijos usados: `docs:` (informe), `proto:` (prototipo), `diag:` (diagramas), `repo:` (organización).
3. Cada apartado tiene un issue. Cerramos el issue cuando el apartado está revisado por otro integrante.
4. Las imágenes van en la carpeta de su apartado (`diagramas/`, `prototipo/...`), con nombres en minúscula y separados por guiones.
5. Los diagramas se editan en el archivo `.dot` y después se regenera el `.png`. No se editan las imágenes a mano.
6. El informe Word se arma al final, a partir de los archivos de `docs/`.

## Decisiones de diseño acordadas

| N° | Decisión | Motivo |
|---|---|---|
| D1 | Problema: reporte de fallas por operarios en planta de packing. | Uno de los integrantes conoce el contexto de primera mano. |
| D2 | Usuario principal: operario de línea (no el técnico). | Es quien hoy no tiene herramienta ni retroalimentación. |
| D3 | Se elige la alternativa B (asistente paso a paso con QR). | Es la que mejor cumple los requisitos (ver tabla comparativa). |
| D4 | Metáfora combinada: asistente paso a paso + seguimiento tipo delivery. | Se basa en experiencias que los usuarios ya conocen. |
| D5 | El color nunca va solo: siempre va con ícono y texto. | Accesibilidad (R11). |
| D6 | Prototipo de media fidelidad en HTML publicado en GitHub Pages. | Se puede abrir con un link, sin instalar nada, y queda versionado en el repo. |
| D7 | Tipografía Atkinson Hyperlegible. | Fue diseñada para lectores con baja visión. |
