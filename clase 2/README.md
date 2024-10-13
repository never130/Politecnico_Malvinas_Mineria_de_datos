##  <font color = 'carmesi'> Introducción a la Limpieza de Datos </font>
La limpieza de datos es un proceso fundamental en el análisis de datos que implica identificar y corregir errores, inconsistencias y valores faltantes en un conjunto de datos. Un conjunto de datos limpio y bien estructurado es esencial para garantizar la validez y la confiabilidad de los resultados del análisis. La limpieza de datos no solo mejora la calidad de los datos, sino que también permite obtener conclusiones más precisas y significativas.

### Resumen de Hallazgos y Técnicas Aplicadas
En mi investigación, me centré en el tratamiento de valores faltantes en el conjunto de datos del Titanic. Al analizar este conjunto, descubrí que varias columnas, como Age, contenían valores NaN, lo que podría comprometer el análisis y llevar a interpretaciones erróneas.

La técnica que apliqué fue la eliminación de filas con valores faltantes en la columna Age. Este enfoque es efectivo cuando la proporción de datos faltantes es baja y no afectará significativamente el tamaño del conjunto de datos. Sin embargo, también existe la opción de imputar estos valores utilizando la media o mediana de la columna, lo que preservaría más datos.

### Mejora en el Análisis de Datos
La aplicación de esta técnica de limpieza de datos mejora el análisis de varias maneras:

1. Reducción de Sesgos: Al eliminar filas con valores faltantes, se evita que estos datos influyan negativamente en los resultados. Esto es crucial para realizar análisis estadísticos precisos y confiables.

2. Aumento de la Calidad de Datos: Un conjunto de datos libre de valores faltantes permite realizar cálculos y visualizaciones sin interrupciones. Las funciones estadísticas, como la media y la mediana, se calcularán de manera más efectiva.

3. Facilidad de Interpretación: Un conjunto de datos limpio facilita la identificación de patrones y tendencias, lo que lleva a conclusiones más claras y significativas sobre el comportamiento de los pasajeros del Titanic.

4. Mejora en Modelado Predictivo: La calidad de los datos es esencial para construir modelos predictivos precisos. Al limpiar los datos, se incrementa la confianza en las predicciones que se realicen con base en ellos.