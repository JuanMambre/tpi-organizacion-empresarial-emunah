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
