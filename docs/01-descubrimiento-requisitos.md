# 1. Descubrimiento de requisitos

## 1.1 Problema de interacción

En las plantas de packing de fruta de la zona central, cuando una máquina de la línea falla (por ejemplo, una calibradora que se atasca o una cinta que hace un ruido extraño), el operario que la detecta normalmente avisa de forma verbal: le grita al supervisor, lo busca caminando o le pide a alguien que llame por radio al taller de mantención. Este aviso "boca a boca" genera varios problemas de interacción:

- La información llega incompleta o distorsionada al técnico ("se echó a perder la máquina de la línea dos"), sin indicar qué máquina, qué síntoma tiene ni si la línea está detenida.
- El operario no recibe ninguna retroalimentación: no sabe si su aviso llegó, si alguien viene en camino o cuánto falta. Esto genera incertidumbre y avisos repetidos.
- No queda registro del aviso, por lo que no se puede saber cuánto se demoró la reparación ni qué máquinas fallan más.

El problema que abordamos no es la falta de un sistema de mantención (muchas empresas ya tienen uno), sino que **el operario de la línea no tiene una forma simple, rápida y confiable de reportar una falla y saber qué pasó con su aviso**. Las herramientas existentes suelen estar pensadas para el técnico o el jefe de mantención, con formularios largos y lenguaje técnico.

## 1.2 Usuarios objetivo

Uno de los integrantes del grupo trabaja en el área de TI de una exportadora de fruta de la región del Maule, lo que nos permitió conocer el contexto de primera mano. Con esa información construimos tres proto-personas. El usuario principal es el operario; el técnico y el supervisor son usuarios secundarios que reciben la información.

| Proto-persona | Rol | Características relevantes para la interacción |
|---|---|---|
| **Rosa, 46 años** (usuaria principal) | Operaria de temporada en la línea 2 | Usa celular Android para WhatsApp y llamadas. Lee bien, pero no le gusta escribir mensajes largos. No conoce los nombres técnicos ni los códigos de las máquinas; las reconoce por su forma o ubicación. Trabaja con guantes y delantal. Su objetivo es "que alguien venga luego" para no perder producción. |
| **Juan, 34 años** | Técnico de mantención | Atiende varias líneas en el turno. Necesita saber qué máquina es, qué síntoma tiene y qué tan urgente es, antes de salir del taller, para llevar la herramienta correcta. |
| **Carla, 39 años** | Supervisora de línea | Responde por la producción de la línea. Necesita enterarse de inmediato cuando la línea se detiene y ver si el reporte ya fue atendido. |

## 1.3 Contexto de uso

- **Físico:** sala de proceso con ruido constante de máquinas, piso mojado, temperatura baja y luz artificial. Los operarios usan guantes de nitrilo o de hilo, lo que dificulta tocar elementos pequeños y escribir.
- **Temporal:** en temporada alta (cerezas y berries) se trabaja con mucha presión de tiempo. Cada minuto con la línea detenida es producción perdida, por lo que el reporte no puede tomar más de un minuto.
- **Tecnológico:** el reporte se haría desde el celular en zonas donde la empresa lo permite o desde una tablet fija por línea (supuesto a validar con la planta). La señal Wi-Fi puede ser débil en algunos sectores.
- **Social:** existe jerarquía (operario → supervisor → mantención). Algunos operarios sienten que "no les corresponde" avisar directo a mantención o temen que los culpen por la falla.
- **Seguridad:** si hay riesgo para una persona, la prioridad es detener la máquina y avisar al supervisor; la aplicación no debe reemplazar ese procedimiento.

## 1.4 Tarea principal

> **Reportar una falla de una máquina de la línea y saber en qué estado está la reparación.**

Subtareas: (1) identificar la máquina, (2) indicar qué le pasa, (3) indicar qué tan grave es, (4) enviar y recibir confirmación, (5) seguir el estado y (6) confirmar que quedó funcionando.

## 1.5 Requisitos iniciales

Siguiendo la lógica de Rogers et al. (2023), relacionamos cada situación observada con un requisito de interacción:

| N° | Situación observada | Requisito de interacción |
|---|---|---|
| R1 | El operario no conoce los códigos ni los nombres técnicos de las máquinas. | El sistema debe identificar la máquina sin que el usuario escriba su nombre o código (por ejemplo, con un código QR pegado en la máquina). |
| R2 | Se trabaja con guantes y apuro. | Los botones deben ser grandes (mínimo 48 px, idealmente 60 px de alto) y la tarea debe hacerse solo con toques, sin escribir. |
| R3 | Escribir una descripción de la falla es lento y difícil. | El problema se debe elegir entre categorías con ícono y texto; la foto y el audio deben ser opcionales. |
| R4 | El técnico no sabe la urgencia del aviso. | El reporte debe incluir siempre la gravedad (línea detenida / funciona con problemas / solo aviso). |
| R5 | El ambiente es ruidoso. | La retroalimentación debe ser visual (y vibración), no depender solo del sonido. |
| R6 | El operario no sabe si su aviso llegó. | Al enviar, el sistema debe mostrar una confirmación clara con número de reporte y el estado actual. |
| R7 | El operario no sabe cuánto falta para que llegue el técnico. | El sistema debe mostrar el seguimiento del reporte por estados y avisar cuando cambie. |
| R8 | El código QR puede estar sucio o despegado. | Debe existir una alternativa para elegir la máquina desde una lista organizada por línea. |
| R9 | Elegir una opción equivocada es fácil con guantes. | Antes de enviar, el usuario debe poder revisar y corregir el reporte. |
| R10 | La reparación a veces queda mal hecha. | El operario debe poder confirmar si la máquina quedó funcionando o reabrir el reporte. |
| R11 | Hay usuarios con distinto nivel de lectura y personas con baja visión. | Lenguaje simple, texto de 17 px o más, alto contraste y no usar solo el color para comunicar estados. |
| R12 | Existe un procedimiento de seguridad. | La pantalla de inicio debe recordar qué hacer si hay riesgo para una persona. |
