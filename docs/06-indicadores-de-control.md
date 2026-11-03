# Entrega 4 · Mecanismos de control

Aplicamos el **proceso de control** visto en la Unidad 4: (1) fijar estándares, (2) medir el desempeño, (3) comparar contra el estándar y (4) corregir los desvíos. Los estándares salen de las metas de la Entrega 2; las mediciones se obtienen de los datos que el propio módulo guarda (diccionario de datos de la Entrega 3).

## Indicadores y estándares de desempeño

| # | Indicador | Fórmula | Estándar | Frecuencia | Fuente | Responsable |
|---|---|---|---|---|---|---|
| I1 | Reducción del tiempo de carga de horas | 1 − (tiempo medio actual ÷ tiempo medio de la línea base) | ≥ 50 % | Mensual | Encuesta de tiempos + RegistroDeHoras | PM |
| I2 | Aceptación de propuestas de horas | registros confirmados sin corrección ÷ registros totales | ≥ 80 % | Semanal | RegistroDeHoras | Coordinador |
| I3 | Tiempo de generación del resumen diario | percentil 95 del tiempo de respuesta | ≤ 10 s | Diaria (automática) | Logs del módulo | Infraestructura / DevOps |
| I4 | Cobertura de sugerencias | tickets con sugerencia ÷ tickets con información suficiente | ≥ 90 % | Semanal | SugerenciaAsignacion, Ticket | Coordinador |
| I5 | Aceptación de sugerencias | sugerencias aceptadas ÷ sugerencias generadas | entre 60 % y 90 % | Semanal | SugerenciaAsignacion | Coordinador |
| I6 | Detección de tickets relacionados | casos detectados ÷ casos identificados por el equipo | ≥ 80 % | Por sprint | Pruebas con casos reales | QA / Testing |
| I7 | Retrabajo en QA | tickets que vuelven de QA ÷ tickets probados | ≤ 20 % | Por sprint | Jira (transiciones de estado) | QA / Testing |
| I8 | Distribución del conocimiento | módulos de Trade 10 con 2 o más desarrolladores con experiencia ÷ módulos totales | ≥ 60 % (en crecimiento) | Trimestral | PerfilTecnico | Team Leader |
| I9 | Cumplimiento del cronograma | semanas de desvío respecto del Gantt | ≤ 1 semana | Semanal | GitHub Projects / Gantt | PM |

**Por qué I5 tiene un techo.** Una aceptación muy baja indica que el modelo recomienda mal; una aceptación cercana al 100 % puede indicar que el Coordinador dejó de revisar y acepta por costumbre, que es justamente la amenaza de *dependencia excesiva de la IA* del FODA. Por eso el estándar es una banda y no un mínimo.

**Línea base.** I1 necesita medir el tiempo actual de carga en Google Sheets antes de implementar el módulo. Esa medición forma parte de la etapa de Análisis del Gantt; no inventamos un valor de partida.

## Tipos de control

| Momento | Control | Ejemplo en el proceso |
|---|---|---|
| **Preventivo** (antes) | Validaciones y permisos | Compuerta «¿Información suficiente?»; acceso al resumen solo para PM y Coordinador. |
| **Concurrente** (durante) | Decisiones humanas sobre la salida del sistema | Compuertas «¿Acepta la sugerencia?» y «¿Propuesta correcta?». |
| **Retroalimentación** (después) | Revisión de indicadores | Revisión semanal de I2, I4, I5 e I7; retrospectiva por sprint. |

## Acciones correctivas

| Desvío | Acción |
|---|---|
| I2 < 80 % | Revisar la lógica de estimación de horas con los casos corregidos por los desarrolladores. |
| I3 > 10 s | Optimizar consultas o cachear datos de Jira; escalar a Infraestructura. |
| I4 < 90 % | Analizar qué datos faltan en los tickets y reforzar la carga en Jira. |
| I5 < 60 % | Analizar los `motivo_rechazo` y ajustar los criterios de recomendación. |
| I5 > 90 % | Auditoría por muestreo: el Team Leader revisa decisiones del Coordinador para confirmar que se siguen evaluando. |
| I7 > 20 % | Reforzar criterios de aceptación y pruebas unitarias antes de pasar a QA. |
| I9 > 1 semana | Repriorizar el backlog y renegociar el alcance del sprint. |

## Auditoría técnica del sistema

- **Trazabilidad:** cada sugerencia guarda ticket, desarrollador recomendado, puntaje, decisión y motivo, para poder reconstruir por qué se asignó cada trabajo.
- **Control de cambios:** todo cambio en la documentación o el código entra por *pull request* con revisión; no se trabaja directo sobre `main`.
- **Seguridad de la información:** acceso por rol; los datos personales de actividad no se usan para evaluar desempeño individual sin conocimiento del equipo.
