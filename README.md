# VA_tarea4
# Octubre está cada vez más frío

Visualización de datos temporales disponible en: https://beta.observablehq.com/@as-garciav/temporal-data-climate-data-from-bogota

Los datos de los pronósticos para los próximos 5 días se encuentran disponibles para su descarga en:
http://www.pronosticosyalertas.gov.co/datos-abiertos-ideam

El set de datos para la visualización consta de 5 días (120 horas) de predicciones para los datos climatológicos en la ciudad de Bogotá. Dichos datos cambian cada hora por lo que se tiene un set no variable de datos "Data.csv" en el presente repositorio.

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
 
 El segundo IDIOM radial line chart para describir la temperatura por horas de cada uno de los días de la semana (los datos preprocesados se encuentran en "TempByDayHour.txt")
- Marcas: Líneas (Para mostrar las tendencias en los cambios de la temperatura por días
- Canales: posición radial de los valores de temperatura - Encode Radial Axis Orientation, Order Align para cada una de las horas del día para generar los segmentos en los que se divide el gráfico radial y respetar el caracter cíclico de los datos. 

## Insights
- La primera gráfica muestra como a medida que van pasando los días la temperatura promedio tiende a disminuir, a pesar de que el cambio en realidad es de menos de 1ºC 
- En cuanto a la distribución por horas (pendiente de graficar) los datos son limitados tanto para el primer como para el segundo día, obteniendo datos de la tarde para el primer día y de la madrugada para el último día, lo que puede estar sesgando que la temperatura promedio en el último sea más baja
- En el gráfico radial se espera observar como la temperatura tiene una tendencia a aumentar hacia el medio día y a disminuir en las noches, siendo similar en los diferentes días.
 
