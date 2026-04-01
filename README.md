# Segmentación de Clientes y Predicción de Valor (RFM) – Proyecto Final Integrador
Este repositorio contiene el código y los recursos para el Proyecto Final Integrador. El objetivo es realizar una segmentación estratégica de clientes mediante técnicas de aprendizaje no supervisado (K-Means) y desarrollar un modelo predictivo para anticipar qué clientes se convertirán en perfiles de "Alto Valor".

## Contenido
###### segmentacion_rfm_ml.ipynb: 
Notebook Jupyter con el flujo completo de limpieza de datos, ingeniería de variables RFM, clustering, validación temporal y optimización de modelos.
###### data/: 
Carpeta destinada al dataset (Online_Retail.csv).
###### README.md: 
Este archivo, con la descripción y guía de ejecución.

## Requisitos
Python 3.11 o superior.

Librerías principales: pandas, numpy, sklearn, matplotlib, seaborn.

## Instalación
Clona o descarga este repositorio.

Crea un entorno virtual (opcional pero recomendado):

python -m venv env
source env/bin/activate

Instala las dependencias necesarias:

pip install pandas numpy scikit-learn matplotlib seaborn

## Flujo del Proyecto
El notebook sigue una metodología dividida en:

### Limpieza y Curaduría: Corrección de formatos de fecha, eliminación de nulos y normalización de registros.

### Análisis RFM: Cálculo de Recencia, Frecuencia (basada en transacciones únicas) y Valor Monetario.

### Segmentación (K-Means):

Identificación de 4 clusters clave: Corporativos/Mayoristas, Clientes Fieles, Ocasionales/Nuevos e Hibernando/Perdidos.

Validación mediante Silhouette Score (0.616).

### Estrategia de Validación Temporal:

División de datos en 9 meses de observación y 3 meses de predicción para evitar la circularidad (Data Leakage).

### Modelado Predictivo:

Comparativa entre Regresión Logística, SVM y Random Forest.

### Optimización mediante GridSearchCV: 
Ajuste de hiperparámetros en Random Forest buscando el equilibrio óptimo entre Precision y Recall.

## Resultados Clave
Modelo Final: Random Forest Optimizado.

ROC-AUC: 0.855, demostrando una alta capacidad de discriminación para predecir futuros clientes VIP.

## Segmentos Identificados:

Cluster 2: Corporativos/Mayoristas (Alta rentabilidad B2B).

Cluster 3: Clientes Fieles (Base recurrente).

Cluster 0: Ocasionales/Nuevos (Potencial de crecimiento).

Cluster 1: Hibernando/Perdidos (Riesgo de abandono).

## Ejecución
Para correr el análisis, abre el notebook y ejecuta las celdas secuencialmente:

Bash
jupyter notebook segmentacion_rfm_ml.ipynb
