# Entrega 4 · Backlog ágil e historias de usuario

El backlog se gestiona en **GitHub Projects** (tablero Kanban con los estados **Por hacer → En progreso → Listo**). Cada historia de usuario es un *issue* del repositorio; los *pull requests* que la resuelven la cierran automáticamente con `Closes #n`, y el tablero la mueve a **Listo**.

## Historias de usuario

- [HU-01 · Propuesta automática de horas](historias/HU-01-propuesta-de-horas.md)
  > **Como** desarrollador, **quiero** que el módulo me proponga las horas trabajadas a partir de los tickets en los que trabajé durante la jornada, **para** registrarlas en menos tiempo y sin olvidos.
- [HU-02 · Sugerencia de asignación de tickets](historias/HU-02-sugerencia-de-asignacion.md)
  > **Como** coordinador de desarrollo, **quiero** recibir una sugerencia de desarrollador para cada ticket nuevo, basada en su experiencia en el módulo afectado y en su disponibilidad, **para** asignar el trabajo con mejor criterio y distribuir el conocimiento del equipo.
- [HU-03 · Resumen diario de actividad](historias/HU-03-resumen-diario.md)
  > **Como** Project Manager, **quiero** obtener un resumen diario de la actividad de cada desarrollador, con los tickets trabajados, los avances y los bloqueos, **para** seguir el proyecto sin depender solo de la daily.

## Trazabilidad

| Historia | Meta | Tarea del BPMN | Entidad de datos |
|---|---|---|---|
| HU-01 | M1 | Generar propuesta de horas · Revisar propuesta de horas | RegistroDeHoras |
| HU-02 | M3, M4 | Generar sugerencia de asignación · Revisar sugerencia · Detectar tickets relacionados | SugerenciaAsignacion, PerfilTecnico |
| HU-03 | M2 | Generar propuesta de horas y resumen diario | RegistroDeHoras, Ticket |
