# Módulo inteligente de gestión y seguimiento del equipo · Emunah

**Trabajo Práctico Integrador y Progresivo · Organización Empresarial**
Tecnicatura Universitaria en Programación a Distancia · Universidad Tecnológica Nacional · 2.º cuatrimestre 2026

| | |
|---|---|
| **Integrante** | Juan Cruz Mambretti |
| **Comisión** | 10 |
| **Docente titular** | Prof. Gabriela Martínez |
| **Tutor** | Cdor. Guillermo Carvajal |
| **Tablero de gestión** | [GitHub Projects · Backlog TPI Emunah](__URL_TABLERO__) |

## Descripción del sistema

**Emunah** es una fintech que desarrolla **Trade 10**, la plataforma que conecta a los bancos con el mercado de capitales (BYMA). Este proyecto propone un **módulo inteligente** para el equipo de desarrollo de Trade 10 que, a partir del historial de Jira y de la actividad diaria:

- **propone la carga de horas** trabajadas, que cada desarrollador confirma o corrige;
- **sugiere a quién asignar cada ticket** según la experiencia y la disponibilidad, y alerta sobre tickets relacionados;
- **genera un resumen diario** de actividad para el Project Manager.

El módulo no reemplaza decisiones humanas: el Coordinador decide la asignación y cada desarrollador valida sus horas.

## Contenido del repositorio

| Documento | Contenido |
|---|---|
| [01 · Organización y enfoque sistémico](docs/01-organizacion-y-enfoque-sistemico.md) | Caso de estudio, misión, visión, modelo TGS y módulo propuesto (Entrega 1). |
| [02 · Diagnóstico y planeación](docs/02-diagnostico-y-planeacion.md) | FODA, FODA cruzado, objetivo, metas y Gantt (Entrega 2). |
| [03 · Estructura formal y datos](docs/03-estructura-formal-y-datos.md) | Organigrama y diccionario de datos (Entrega 3). |
| [04 · Proceso BPMN](docs/04-proceso-bpmn.md) | Modelo BPMN 2.0 del proceso de gestión de tickets (Entrega 4). |
| [05 · Backlog e historias de usuario](docs/05-backlog-historias-de-usuario.md) | Las tres historias de usuario y su trazabilidad (Entrega 4). |
| [06 · Indicadores de control](docs/06-indicadores-de-control.md) | Estándares de desempeño, indicadores y acciones correctivas (Entrega 4). |
| [`diagramas/`](diagramas) | Organigrama, BPMN en PNG y archivo editable `.bpmn`. |

## Cómo trabajamos en este repositorio

- `main` contiene solo trabajo revisado. Cada tema se desarrolla en una **rama secundaria** (`docs/…`, `feature/…`) y se integra con un **pull request** revisado.
- Los commits siguen el formato `tipo(alcance): descripción` en español (por ejemplo, `docs(bpmn): agrega compuertas de excepción`).
- Cada historia de usuario es un *issue* vinculado al tablero; el pull request que la resuelve la cierra con `Closes #n`.

## Declaración de uso de IA

**Herramienta.** Usé **Claude** (asistente de IA de Anthropic) a través de **Claude Code**, un entorno que trabaja sobre los archivos de mi computadora y con el que el asistente puede ejecutar comandos.

**Para qué la usé.** Para estructurar el README y los documentos de `docs/`, para escribir el código Python que dibuja el diagrama BPMN y genera el archivo `.bpmn`, para proponer el set de indicadores de control, para ejecutar los comandos de Git y para armar el PDF consolidado.

**Prompt principal y contexto.** El pedido fue directo: *«necesitamos hacer y entregar el TPI 4 de Org. Empresarial»*. Lo que hizo que el resultado no fuera genérico fue el contexto que el asistente tuvo que leer antes de producir nada: la consigna oficial y la rúbrica de la Entrega 4, mis Entregas 1, 2 y 3 y las devoluciones del tutor de cada una. Por eso el proceso modelado, las historias y los indicadores se apoyan en las metas (M1 a M5) y en las entidades que ya había definido, y se incorporaron las observaciones pendientes (FODA cruzado, dificultades de implementación y una declaración de IA más concreta).

**Decisiones propias.**
- El caso, los roles y el circuito real de trabajo (tickets por Jira, daily, horas en Google Sheets) salen de mi experiencia en Emunah y ya estaban en la Entrega 1.
- Elegí publicar con mi cuenta personal de GitHub y firmar los commits con mi correo personal y no con el corporativo, para no exponer datos de la empresa en un repositorio público.
- Elegí GitHub Projects en lugar de Jira para que historias, ramas y pull requests queden vinculados en un solo lugar.

**Errores de la IA que se corrigieron.**
- Al resumir la Entrega 3, el asistente reescribió el diccionario de datos con nombres y tipos de campos que **no coincidían** con el original (por ejemplo, `idTicket` como String en lugar de `id_ticket` Integer). Se contrastó contra el documento entregado y se reemplazó por las tablas exactas.
- La primera versión del diagrama BPMN tenía textos superpuestos con los íconos de las tareas y una etiqueta tapada por un flujo de mensaje; se corrigió tras revisar las imágenes.
- Para el indicador de tiempo de carga de horas era fácil «inventar» una línea base (por ejemplo, 15 minutos por día). Se decidió no poner un número sin datos y dejar la medición como parte de la etapa de Análisis.

**Responsabilidad.** Revisé el contenido y lo puedo defender en el coloquio; cualquier error que haya quedado es mío y no del asistente.
