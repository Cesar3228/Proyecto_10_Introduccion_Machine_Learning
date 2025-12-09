# Proyecto_10_Introduccion_Machine_Learning

# Proyecto 10 – Clasificación de planes de tarifa Megaline  
# Project 10 – Megaline Tariff Plan Classification

---

## 🧩 Descripción general / Overview

### 🇪🇸 Español

La compañía de telefonía móvil **Megaline** busca reducir el uso de planes heredados y promover sus nuevos planes **Smart** y **Ultra**.  
Para apoyar esta estrategia, en este proyecto se desarrolló un **modelo de clasificación** capaz de recomendar el plan más adecuado para cada cliente a partir de su comportamiento mensual de uso.

El objetivo principal del proyecto es construir un modelo predictivo con una **exactitud mínima de 0.75**, utilizando datos reales de clientes que ya migraron a los nuevos planes.

Este proyecto forma parte del **Sprint 10 – Clasificación** del programa de **Data Science de TripleTen**.

---

### 🇬🇧 English

The mobile company **Megaline** wants to reduce the use of legacy plans and promote its new **Smart** and **Ultra** plans.  
To support this strategy, a **classification model** was built to recommend the most suitable plan for each customer based on their monthly usage behavior.

The main goal of the project is to develop a predictive model with a **minimum accuracy of 0.75**, using real data from customers who have already switched to the new plans.

This project is part of **Sprint 10 – Classification** in the **TripleTen Data Science program**.

---

## 📂 Datos / Data

### Archivo principal / Main file
- Ruta / Path: `/datasets/users_behavior.csv`

Cada observación corresponde al comportamiento mensual de un usuario.

### Variables / Features
- `calls` — número de llamadas / number of calls  
- `minutes` — duración total de llamadas (minutos) / total call duration (minutes)  
- `messages` — número de mensajes SMS / number of SMS messages  
- `mb_used` — tráfico de internet usado (MB) / internet traffic used (MB)  
- `is_ultra` — plan actual: **Ultra = 1**, **Smart = 0**

---

## 🔍 Metodología / Methodology

### 🇪🇸 Español

1. **Carga y exploración de datos**
   - Lectura del archivo CSV.
   - Revisión de tipos de datos, valores ausentes y distribución de variables.

2. **Preparación de los datos**
   - Separación de variables predictoras y variable objetivo (`is_ultra`).
   - Segmentación del dataset en conjuntos de **entrenamiento**, **validación** y **prueba**.

3. **Entrenamiento de modelos**
   - Entrenamiento de distintos modelos de clasificación.
   - Ajuste de hiperparámetros utilizando el conjunto de validación.

4. **Evaluación del modelo**
   - Comparación de modelos mediante la métrica de **accuracy**.
   - Selección del mejor modelo según desempeño y robustez.

5. **Prueba de cordura**
   - Comparación del modelo final contra una estrategia ingenua (baseline) para asegurar que el modelo aprende patrones reales.

---

### 🇬🇧 English

1. **Data loading and exploration**
   - Reading the CSV file.
   - Checking data types, missing values, and feature distributions.

2. **Data preparation**
   - Separating features and target variable (`is_ultra`).
   - Splitting the data into **training**, **validation**, and **test** sets.

3. **Model training**
   - Training different classification models.
   - Hyperparameter tuning using the validation set.

4. **Model evaluation**
   - Comparing models using **accuracy** as the main metric.
   - Selecting the best-performing and most robust model.

5. **Sanity check**
   - Comparing the final model against a naive baseline to ensure it captures real patterns.

---

## 🤖 Modelos y Resultados / Models and Results

### 🇪🇸 Español

### Modelos evaluados
- **DecisionTreeClassifier**
- **RandomForestClassifier**
- **LogisticRegression**

### Resultados de exactitud (accuracy)

| Modelo                    | Accuracy |
|---------------------------|----------|
| DecisionTreeClassifier    | 0.795 |
| RandomForestClassifier    | 0.815 |
| LogisticRegression        | 0.744 |

El modelo con mejor desempeño fue **RandomForestClassifier**, superando el umbral mínimo requerido de **0.75**.

### Evaluación en el conjunto de prueba
El modelo final obtuvo:

- **Accuracy en prueba:** **0.80**

Métricas detalladas por clase:

- **Plan Smart (0):**
  - Precision: 0.82  
  - Recall: 0.92  
  - F1-score: 0.87  

- **Plan Ultra (1):**
  - Precision: 0.74  
  - Recall: 0.53  
  - F1-score: 0.62  

Estos resultados muestran que el modelo identifica correctamente la mayoría de los usuarios del plan Smart y mantiene un desempeño aceptable para los usuarios del plan Ultra.

### Prueba de cordura
El modelo entrenado supera claramente estrategias de clasificación ingenuas, demostrando que aprende patrones relevantes del comportamiento de los clientes.

---

### 🇬🇧 English

### Evaluated models
- **DecisionTreeClassifier**
- **RandomForestClassifier**
- **LogisticRegression**

### Accuracy results

| Model                     | Accuracy |
|---------------------------|----------|
| DecisionTreeClassifier    | 0.795 |
| RandomForestClassifier    | 0.815 |
| LogisticRegression        | 0.744 |

The best-performing model was **RandomForestClassifier**, exceeding the required accuracy threshold of **0.75**.

### Test set evaluation
The final model achieved:

- **Test accuracy:** **0.80**

Detailed metrics by class:

- **Smart plan (class 0):**
  - Precision: 0.82  
  - Recall: 0.92  
  - F1-score: 0.87  

- **Ultra plan (class 1):**
  - Precision: 0.74  
  - Recall: 0.53  
  - F1-score: 0.62  

These results indicate strong performance for identifying Smart plan users and reasonable performance for Ultra plan users.

### Sanity check
The trained model clearly outperforms naive baseline strategies, confirming that it captures meaningful patterns from customer usage data.

---

## 📁 Estructura del repositorio / Repository Structure

```text
.
├── Proyecto_10.ipynb
├── requirements.txt
└── README.md
