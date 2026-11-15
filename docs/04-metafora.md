# 4. Metáfora de interfaz

Usamos una **metáfora combinada**, porque la tarea tiene dos momentos distintos:

1. **Asistente paso a paso** para crear el reporte. Es como cuando un supervisor le pregunta al operario "¿qué máquina?, ¿qué le pasa?, ¿está parada?": una pregunta a la vez y en orden.
2. **Seguimiento de un pedido de delivery** para después de enviar. La mayoría de los usuarios ya ha usado una app de delivery o seguido un envío, así que entiende sin explicación una línea de estados como "Recibido → En camino → Entregado". Nosotros la adaptamos a "Recibido → Técnico en camino → Reparado".

Elegimos estas metáforas porque se basan en experiencias que nuestros usuarios ya conocen. Así reducen lo que deben aprender y responden a la principal molestia del operario: no saber qué pasó con su aviso.

| Elemento de la metáfora | Relación con la experiencia conocida | Aplicación en la interfaz |
|---|---|---|
| Preguntas en orden | El supervisor pregunta una cosa a la vez. | Pasos 1, 2 y 3 con barra de avance y "Paso 2 de 3". |
| Número de pedido | En el delivery el pedido tiene un número para identificarlo. | Cada reporte recibe un N° (R-0142) que se muestra al enviar. |
| Línea de estados | "Preparando → En camino → Entregado". | Enviado → Recibido → Técnico en camino → Reparado, con hora de cada cambio. |
| "Tu repartidor llega en 5 min" | Tiempo estimado de llegada. | "Técnico en camino · Llegada estimada: 5 min". |
| Chat con el repartidor | Mensajes cortos con quien viene. | Mensajes con el técnico usando respuestas rápidas. |
| "¿Cómo estuvo tu pedido?" | Confirmación al final del servicio. | "¿La calibradora funciona bien?" Sí / No, sigue fallando. |

**Límite de la metáfora:** en un delivery el usuario no puede hacer nada mientras espera. En ReportaYa el operario sí puede agregar información (foto, audio o mensajes), lo que es una diferencia que hay que dejar clara en la pantalla de detalle. Además, la metáfora no aplica cuando hay riesgo para una persona: ahí se debe seguir el procedimiento de seguridad y no "esperar el pedido". Por eso agregamos el aviso de seguridad en la pantalla de inicio.
