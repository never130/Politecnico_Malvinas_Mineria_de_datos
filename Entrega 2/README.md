# Análisis de Datos del Conjunto Adult

Este proyecto realiza un análisis exploratorio y limpieza de datos del conjunto `adult_data.csv`, que contiene información socioeconómica y demográfica de personas en relación con sus ingresos. El objetivo es entender las características de los datos y las relaciones entre las variables, especialmente aquellas relacionadas con la variable objetivo `Class` (ingresos `>50K` o `<=50K`).

## Contenido

- [Descripción del Proyecto](#descripción-del-proyecto)
- [Requisitos](#requisitos)
- [Estructura del Código](#estructura-del-código)
- [Pasos del Análisis](#pasos-del-análisis)
- [Visualización de Resultados](#visualización-de-resultados)
- [Conclusiones](#conclusiones)

## Descripción del Proyecto

Este análisis explora relaciones entre variables como `Age` (edad), `Eduction_num` (nivel educativo), `Hours_per_week` (horas trabajadas por semana) y la `Clase de Ingreso` (Class). Las visualizaciones ayudan a identificar patrones y diferencias en la distribución de estas variables entre individuos con ingresos `<=50K` y `>50K`.

## Requisitos

Para ejecutar el análisis, necesitas instalar las siguientes bibliotecas en Python:

```
pip install pandas seaborn matplotlib scikit-learn numpy
```

## Estructura del Código
1. Carga y Exploración de Datos:

- Carga el archivo CSV.
- Muestra las primeras filas para entender el formato de los datos.
- Imprime estadísticas descriptivas y verifica datos faltantes y valores únicos en columnas categóricas.
  
2. Limpieza de Datos:

- Reemplazo de Valores Faltantes: Las columnas numéricas se rellenan con el valor promedio, mientras que las categóricas se completan con "Unknown".
- Corrección de Errores Tipográficos: Se renombra la columna Rice a Race.
- Eliminación de Outliers: Se utiliza el rango intercuartílico (IQR) para filtrar valores atípicos en las columnas Capital_gain, Capital_loss, Age, Eduction_num, y Hours_per_week.

3. Estandarización de Variables:

Las columnas numéricas (Age, Eduction_num, Hours_per_week) se escalan mediante StandardScaler para tener una media de 0 y desviación estándar de 1, con el fin de preparar los datos para modelado en futuras etapas.

## Pasos del Análisis
1. Análisis Descriptivo Inicial
- Exploración general y descripción estadística de los datos.
- Verificación y reemplazo de valores faltantes.
  
2. Limpieza y Transformación de Datos
- Corrección de nombres de columnas y reemplazo de valores tipográficos.
- Eliminación de outliers en columnas seleccionadas.
- Estandarización de variables numéricas para análisis comparativo y visualización.
  
3. Visualización de Resultados
Para visualizar relaciones entre variables y la Clase de Ingreso, se utilizaron diagramas de cajas (boxplots) y violin plots:

- Distribución de Edad según Clase de Ingreso: Para ver si existe una relación entre la edad y los ingresos.
- Distribución del Nivel Educativo según Clase de Ingreso: Para analizar si el nivel educativo tiene impacto en los ingresos.
- Distribución de Horas Trabajadas por Semana según Clase de Ingreso: Para examinar si las personas que ganan más tienden a trabajar más horas.
  
### Ejemplo de código para los gráficos
```
# Diagrama de cajas para Edad por Clase de Ingreso
plt.figure(figsize=(10, 6))
sns.boxplot(x='Class', y='Age', data=df_clean, palette='viridis')
plt.title("Distribución de Edad según Clase de Ingreso", fontsize=18)
plt.xlabel("Clase de Ingreso", fontsize=16)
plt.ylabel("Edad", fontsize=16)
plt.show()
```

## Conclusiones
Este análisis proporciona una vista detallada de cómo variables como Edad, Nivel Educativo y Horas Trabajadas están distribuidas en función de los ingresos. En general, se observa que:

>Los ingresos tienden a ser más altos en personas de mayor edad y nivel educativo.
Las personas que ganan más tienden a trabajar más horas por semana, aunque existen excepciones.

Ever Loza, Mineria de Datos, Centro Politecnico Superior Malvinas Argentinas