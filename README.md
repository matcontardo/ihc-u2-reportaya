# ReportaYa 🔧: reporte de fallas para operarios de planta

Trabajo grupal de la **Unidad 2** de *Interacción Humano Computador*, Ingeniería en Computación e Informática, Universidad Mayor.

**ReportaYa** es una propuesta de app móvil para que los operarios de una planta de packing de fruta reporten la falla de una máquina en menos de un minuto (escaneando un código QR y respondiendo 3 preguntas con botones grandes) y puedan **seguir el estado de la reparación**, como si siguieran un pedido de delivery.

👉 **Ver prototipo navegable:** https://matcontardo.github.io/ihc-u2-reportaya/prototipo/media-fidelidad/

📄 **Resumen de la entrega:** [RESUMEN.md](RESUMEN.md)

## Integrantes

- Matías Contardo
- Daniela Geell
- Francisco Ocares

## Proceso de diseño

| Apartado | Documento |
|---|---|
| 1. Descubrimiento de requisitos | [docs/01-descubrimiento-requisitos.md](docs/01-descubrimiento-requisitos.md) |
| 2. Diseño de alternativas | [docs/02-alternativas.md](docs/02-alternativas.md) |
| 3. Modelo conceptual | [docs/03-modelo-conceptual.md](docs/03-modelo-conceptual.md) |
| 4. Metáfora de interfaz | [docs/04-metafora.md](docs/04-metafora.md) |
| 5. Tipos de interacción | [docs/05-tipos-interaccion.md](docs/05-tipos-interaccion.md) |
| 6. Arquitectura de información y flujo | [docs/06-arquitectura-flujo.md](docs/06-arquitectura-flujo.md) |
| 7. Diseño visual y emocional | [docs/07-diseno-visual-emocional.md](docs/07-diseno-visual-emocional.md) |
| 8. Prototipado | [docs/08-prototipado.md](docs/08-prototipado.md) |
| 9. Uso de GitHub | [docs/09-uso-github.md](docs/09-uso-github.md) |
| Acuerdos del equipo | [docs/acuerdos-equipo.md](docs/acuerdos-equipo.md) |
| Bitácora | [docs/bitacora.md](docs/bitacora.md) |
| Informe final (Word) | [informe/](informe/) |

## Estructura del repositorio

```
ihc-u2-reportaya/
├── README.md
├── RESUMEN.md                 # archivo resumen de la entrega
├── docs/                      # un archivo por apartado + acuerdos + bitácora
├── diagramas/                 # .dot (Graphviz) y .png
├── prototipo/
│   ├── baja-fidelidad/        # bocetos alternativas A, B y C
│   └── media-fidelidad/       # index.html navegable + capturas/
└── informe/                   # informe final .docx
```

## Cómo ver el prototipo en local

Abre `prototipo/media-fidelidad/index.html` en cualquier navegador. Para ir directo a una pantalla, agrega `?nombre` a la URL, por ejemplo `index.html?gravedad` o `index.html?misreportes&notif`.

Para regenerar los diagramas se usa [Graphviz](https://graphviz.org/):

```bash
cd diagramas
dot -Tpng -Gdpi=160 flujo-usuario.dot -o flujo-usuario.png
```

## Referencia principal

Rogers, Y., Sharp, H. & Preece, J. (2023). *Interaction design: Beyond human-computer interaction* (6ª ed.). Wiley.
