# Life Expectancy Prediction

### Descripción del proyecto

El objetivo de este proyecto es predecir la esperanza de vida de un país, analizando datos de 193 países entre 2000 y 2015, combinando información del Observatorio Global de Salud de la OMS y datos económicos de la ONU. El conjunto de datos incluye 22 variables clasificadas en factores de inmunización, mortalidad, económicos y sociales. 

### Fuentes de dato

La base de datos utilizada para este proyecto se encuentra en el archivo "Life Expectancy Data.csv", conteniendo registros de países por año.

### Herramientas

- Python - EDA y modelamiento

### Limpieza / preparación de datos

En la fase inicial de preparación de datos, se hizo lo siguiente:
1. Carga de data e inspección.
2. Validación de datos duplicados.
3. Validación de datos nulos e imputación con Iterative Imputer.
4. Análisis de correlación de variables, eliminando variables sin correlación significativa con la variable objetivo.

### Modelamiento de datos

Se probaron diversos escaladores y modelos de Machine Learning para validar el mejor rendimiento para el proyecto.

- Escaladores: Standard Scaler, Min Max Scaler y Robust Scaler.
- Modelos: Regresión Lineal, XGBoost, Random Forest y Extra Trees Regressor.

### Resultados

Los resultados de este proyecto son:
1. El modelo con mejor rendimiento fue utilizando un escalador MinMax Scaler y luego un modelo de Extra Trees Regressor.
2. Se optimizaron los hiperparámetros del modelo con los valores: {'max_depth': None, 'min_samples_leaf': 1, 'min_samples_split': 2, 'n_estimators': 200}
3. Se obtuvo un MSE = 1.84.
4. Se obtuvo un R2 = 0.98
