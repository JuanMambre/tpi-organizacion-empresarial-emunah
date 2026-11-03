# Entrega 1 · La organización y su enfoque sistémico

> Síntesis de la Entrega 1 del TPI. El documento completo está en el PDF consolidado.

## Caso de estudio

**Emunah** es una empresa fintech que desarrolla soluciones tecnológicas para entidades financieras. Su único producto, **Trade 10**, conecta a los bancos con el mercado de capitales (BYMA) y centraliza parte de su operatoria bursátil.

| | |
|---|---|
| **Misión** | Facilitar y optimizar la operatoria de las entidades bancarias mediante soluciones tecnológicas aplicadas al mercado financiero. |
| **Visión** | Ampliar el alcance de Trade 10 hacia otros mercados de la región (Brasil, Chile) y, a largo plazo, integrarse con plazas financieras globales. |
| **Sector** | Cuaternario (conocimiento, tecnología e información), dentro del ecosistema fintech. |

## Emunah como sistema abierto (TGS)

| Componente | Contenido |
|---|---|
| **Entradas** | Bancos clientes, conocimiento de los empleados, instrucciones y datos de los sistemas de los bancos (Bantotal), datos del mercado (precios, cotizaciones, estados), órdenes de los clientes finales. |
| **Procesos** | Recepción, procesamiento y transmisión de operaciones entre los bancos y el mercado; desarrollo, mantenimiento y soporte de Trade 10. |
| **Salidas** | Resultados y estados de las operaciones, posiciones, información operativa para los bancos. |
| **Ambiente** | Bancos, BYMA, BCRA, CNV, competidores (por ejemplo Nasdaq Calypso). |
| **Retroalimentación** | Incidentes y solicitudes de cambio de los bancos que ingresan por Jira → Project Manager → Team Leader y Coordinador → equipo de desarrollo. |
| **Límites** | Dentro: Trade 10, empleados y procesos internos. Fuera: bancos, Bantotal, BYMA, reguladores y mercado. |

## Módulo propuesto

**Módulo inteligente de gestión y seguimiento del equipo**: una herramienta con IA que toma información de Jira y de la actividad laboral para:

- proponer la carga de horas trabajadas (hoy se hace a mano en Google Sheets), que el desarrollador revisa y confirma;
- generar un resumen diario de actividad para el Project Manager;
- sugerir al Coordinador qué desarrollador tiene mejores antecedentes para cada ticket, construyendo un perfil técnico progresivo;
- detectar tickets que afectan una misma pantalla o componente para evitar conflictos.

La decisión final siempre queda en manos de las personas: el módulo es un apoyo, no un reemplazo.
