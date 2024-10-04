# Vanguard Digital Experiment Analysis

## Descripción

Este proyecto tiene como objetivo analizar los resultados de un experimento digital realizado por Vanguard para evaluar la efectividad de una nueva interfaz de usuario (UI). El propósito de la nueva UI es mejorar la experiencia del usuario y aumentar las tasas de finalización del proceso en línea mediante indicaciones contextuales oportunas.

## Estructura del Proyecto

### 1. Datos Utilizados
- **Perfiles de Clientes (df_final_demo)**: Datos demográficos como edad, sexo y detalles de la cuenta.
- **Huellas Digitales (df_final_web_data)**: Registro detallado de las interacciones en línea de los clientes, dividido en pt_1 y pt_2.
- **Lista de Experimentos (df_final_experiment_clients)**: Identifica los clientes que participaron en el experimento y el grupo al que pertenecen.

### 2. Proceso de Limpieza y Fusión de Datos
- **Eliminación de Duplicados**: `df.drop_duplicates()`
- **Imputación de Valores Faltantes**: `SimpleImputer(strategy='median')`
- **Conversión de Tipos de Datos**: `pd.to_numeric(errors='coerce')`
- **Fusión de Datos**: `pd.concat()`, `pd.merge()`

### 3. Análisis Exploratorio de Datos (EDA)
- **Distribución de la Edad de los Clientes**
- **Tiempo en Navegación**
- **Tasas de Finalización**

### 4. Modelado y Evaluación de Hipótesis
- **Prueba A/B**: Evaluar diferencias entre el grupo de control y el grupo de prueba.
- **Prueba de Hipótesis**: Comparar tasas de finalización entre grupos.
- **Métricas de Rendimiento**: Precisión, Recall, F1-Score, AUC-ROC

### 5. Conclusiones y Recomendaciones
- **Implementar la Nueva Interfaz**
- **Monitoreo Continuo y Recopilación de Feedback**
- **Escalabilidad y Personalización**

## Estructura de Directorios

```plaintext
Vanguard-Digital-Experiment-Analysis/
├── data/
│   ├── df_final_demo.csv
│   ├── df_final_web_data_pt_1.csv
│   ├── df_final_web_data_pt_2.csv
│   └── df_final_experiment_clients.csv
├── notebooks/
│   ├── data_cleaning.ipynb
│   ├── eda.ipynb
│   ├── modeling.ipynb
│   └── results.ipynb
├── src/
│   ├── data_cleaning.py
│   ├── eda.py
│   ├── modeling.py
│   └── utils.py
├── README.md
└── requirements.txt
