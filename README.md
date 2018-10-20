# VA_tarea4
Vizualization of temporal data, climate information for Bogota, predicted by IDEAM

Los datos de los pronósticos para los próximos 5 días se encuentran disponibles para su descarga en:
http://www.pronosticosyalertas.gov.co/datos-abiertos-ideam

El set de datos para la visualización consta de una semana de predicciones para los datos climatológicos en la ciudad de Bogotá. Dichos datos fueron captados en varios días generando el archivo fuente de información "Data.tsv" del presente repositorio ya que cambian permanentemente y muestran los pronósticos por horas de los siguientes 5 días únicamente.

## What?
Tabla con datos climatológicos y series de tiempo por días de la semana y por horas del día

 - Tipos de datos de interés para la visualización:
 -- Fecha: Contiene 3 variables Año, Mes, Día): Año es cuantitativa secuencial, Mes y Día son Ordinales Cuantitativos cíclicos
 -- Hora: Ordinal Cuantitativo Cíclico
 -- Temperatura: Ordinal Cuantitativa divergente
 
 ## Why?
 Tarea principal: Observar cuál es el pronóstico de la temperatura de Bogotá en los próximos días del mes de Octubre (Tamara = Present:distribution)
 
 Tareas secundarias: 
 - Identificar el dìa con el pronóstico de la mayor y la menor temperatura (Tamara = Identify:Outliers)
 - (pendiente en la viz) Mostrar los cambios de temperatura por hora cada día (Tamara = derive:features)
 - Identificar la variación promedio de la temperatura para los próximos días (Tamara = Locate:features)
 - Describir la tendencia de la temperatura en Bogotá para los próximos días (Tamara = Identify:trends)
 
 ## How?
 Dos gráficos interconectados por el día de la semana analizado
 
 El primer IDIOM dot and linechart para describir la temperatura promedio de cada día (calculada previamente como parte del procesamiento de los datos para obtener la tabla de "AverageTemperature.txt")
 - Marcar: Líneas y Puntos --> El primero para detallar los cambios en la temperatura por días, el segundo para hacer énfasis en el dato de la temperatura para cada día.
 - Canales: posición en x los números de los días de la semana para su uso en un <Arrange-Tables Express>, posición en y de la temperatura en ªC (ninguno de los datos llega temperaturas inferiores a los 10ªC) tambien con un Encode Arrange Tables Express
 - Encode => Express
 
