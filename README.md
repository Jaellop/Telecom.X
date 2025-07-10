# Análisis de Cancelación de Clientes en Telecom.x

## Objetivo

Este análisis tiene como finalidad identificar si existe una correlación entre los usuarios que cancelaron el servicio de Telecom.x en los últimos 72 meses y los servicios que tenían contratados. El objetivo es proponer estrategias que mejoren la retención de usuarios y reduzcan pérdidas económicas.

## Preparación de los datos

- Se limpiaron valores vacíos en la columna `Churn` eliminando espacios en blanco con `.strip()`.
- Se eliminaron valores inválidos en la columna `charges_total` (dentro del diccionario `account`) usando `.isna()`.
- Se ajustó el índice para trabajar con 7032 filas válidas, en lugar de las 7266 originales.

## Análisis realizado

Se exploraron las proporciones de cancelación en función de las variables categóricas:

También se generaron tablas cruzadas y gráficas de barras apiladas para analizar la relación entre la cancelación (`Churn`) y:
- `gender`, `partner`, `dependents`
- `PaperlessBilling`, `senior`
- `PhoneService`, `StreamingTV`, `StreamingMovies`
- `NoInternetService`

## Principales hallazgos

- **Contratos mensuales** presentan una mayor tasa de cancelación. Promover contratos largos con beneficios puede reducirla.
- La mayoría de las cancelaciones provienen de usuarios **menores de 65 años**.
- El **género no influye** significativamente en la cancelación.
- Un **25.21%** de los clientes sin dependientes cancelan. Se recomienda diseñar campañas que refuercen el valor personal del servicio.
- Los usuarios con **factura electrónica** tienden a cancelar más.
- Los servicios de **Streaming TV** tienen mayor cancelación que los de películas.
- Clientes con **solo un mes** de antigüedad representan el 20.90% y cancelan con más frecuencia.
- La probabilidad de cancelación disminuye después de los **38 meses**.
- Clientes que cancelan pagan en promedio **$0.44 más por día**, lo que representa una pérdida económica acumulada.
- Contratos largos aseguran ingresos más altos y estables.

## Conclusión

Los resultados permiten identificar patrones claros de cancelación y ofrecen puntos de partida para diseñar estrategias enfocadas en la retención, especialmente durante los primeros meses del cliente y en los servicios con mayor rotación.
