# Resumen de la entrega: ReportaYa

**Asignatura:** Interacción Humano Computador, Unidad 2 · **Carrera:** Ingeniería en Computación e Informática, Universidad Mayor
**Integrantes:** Matías Contardo, [Integrante 2], [Integrante 3]
**Repositorio:** https://github.com/matcontardo/ihc-u2-reportaya
**Prototipo:** https://matcontardo.github.io/ihc-u2-reportaya/prototipo/media-fidelidad/

| Apartado | Resultado principal | Evidencia |
|---|---|---|
| 1. Requisitos | **Problema:** los operarios avisan las fallas de máquinas de forma verbal; la información llega incompleta y el operario no sabe si alguien viene. **Usuario:** operario de línea (proto-persona Rosa) y, como usuarios secundarios, el técnico y la supervisora. **Contexto:** ruido, guantes, apuro y señal débil. **Tarea:** reportar una falla y saber el estado de la reparación. Se definieron 12 requisitos. | `docs/01` |
| 2. Alternativas | A) formulario único, B) asistente paso a paso con QR y C) chatbot. Se elige la **B** porque identifica la máquina sin escribir, se usa con guantes y toma menos de 1 minuto. | `docs/02`, bocetos |
| 3. Modelo conceptual | Conceptos: máquina, línea, reporte, problema, gravedad, estado y aviso. Dos momentos: crear el reporte (3 pasos) y seguirlo (4 estados). | `docs/03`, diagrama |
| 4. Metáfora | **Asistente paso a paso + seguimiento de delivery** (N° de reporte, "Técnico en camino · 5 min", "¿Funciona bien?"). | `docs/04` |
| 5. Tipos de interacción | Instruir (principal), manipular (QR, audio), explorar (lista, mis reportes), conversar (respuestas rápidas) y responder (aviso de reparación). Interfaz móvil, táctil y multimodal. | `docs/05` |
| 6. AI y flujo | 3 secciones (Reportar / Mis reportes / Perfil), etiquetas cotidianas y flujo con caminos alternativos, error y cierre. Camino feliz: 5 toques. | `docs/06`, mapa y flujo |
| 7. Visual y emocional | Botones de 60 px o más, una acción por pantalla, color + ícono + texto y tipografía Atkinson Hyperlegible. Diseño emocional que busca tranquilidad, confianza y control (visceral, conductual y reflexivo). | `docs/07`, capturas |
| 8. Prototipo | Bocetos en baja fidelidad y prototipo **navegable de media fidelidad** con 13 pantallas, en HTML y publicado en GitHub Pages. | `prototipo/` |
| 9. GitHub | Commits por etapa, issues por apartado, acuerdos del equipo, bitácora y release `v1.0-entrega-u2`. | este repositorio |

**Próximo paso:** evaluar el prototipo con 3 a 5 operarios (eficacia, eficiencia, comprensión y satisfacción) y validar el dispositivo que se usará en la planta.
