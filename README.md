# Proyecto_10_Introduccion_Machine_Learning

Clasificación de planes de tarifa Megaline  
Megaline Tariff Plan Classification

---

## 🧩 Descripción general / Overview

**ES 🇪🇸**

La compañía de telefonía móvil **Megaline** quiere que sus clientes dejen de usar planes heredados y migren a sus nuevos planes **Smart** y **Ultra**.  
Para apoyar esta transición, se desarrolló un **modelo de clasificación** que, a partir del comportamiento de uso mensual de cada cliente, recomiende el plan más adecuado.

El objetivo del proyecto es:

- Construir un modelo que prediga si un cliente debe usar el plan **Smart (0)** o **Ultra (1)**.
- Alcanzar una **exactitud mínima (accuracy) de 0.75** en el conjunto de prueba.
- Comparar varios modelos y ajustar sus hiperparámetros.
- Realizar una “prueba de cordura” (sanity check) comparando el modelo elegido contra una estrategia ingenua.

Este proyecto forma parte del **Sprint 10 – Clasificación** del bootcamp de **TripleTen (Data Science)**.

---

**EN 🇬🇧**

The mobile company **Megaline** wants customers to stop using legacy plans and move to the new **Smart** and **Ultra** plans.  
To support this transition, we developed a **classification model** that recommends the most suitable plan based on each customer’s monthly usage behavior.

The project goals are:

- Build a model that predicts whether a customer should use the **Smart (0)** or **Ultra (1)** plan.
- Reach a **minimum accuracy of 0.75** on the test set.
- Compare several models and tune their hyperparameters.
- Perform a **sanity check** by comparing the chosen model to a naive baseline.

This project is part of **Sprint 10 – Classification** from the **TripleTen (Data Science)** bootcamp.

---

## 📂 Datos / Data

**Archivo principal / Main file**

Ruta: `/datasets/users_behavior.csv`

Cada fila representa el comportamiento mensual de un usuario.

**Columnas / Columns**

- `calls` — número de llamadas / number of calls  
- `minutes` — duración total de las llamadas en minutos / total call duration in minutes  
- `messages` — número de SMS / number of SMS messages  
- `mb_used` — tráfico de internet usado en MB / internet traffic used in MB  
- `is_ultra` — plan del mes actual: **1 = Ultra**, **0 = Smart**

---

## 🔍 Metodología / Methodology

**ES 🇪🇸**

Los pasos principales del proyecto fueron:

1. **Carga y revisión de datos**
   - Lectura del archivo `users_behavior.csv`.
   - Inspección de tipos de datos, valores ausentes y distribución de las características.

2. **Preparación de los datos**
   - Separación de las características (`calls`, `minutes`, `messages`, `mb_used`) y la variable objetivo (`is_ultra`).
   - División en conjuntos de **entrenamiento**, **validación** y **prueba**.

3. **Entrenamiento de modelos**
   - Entrenamiento de varios modelos de clasificación (por ejemplo, árboles de decisión, random forest, regresión logística, etc.).
   - Búsqueda de hiperparámetros (profundidad del árbol, número de estimadores, etc.) usando el conjunto de validación.

4. **Evaluación**
   - Cálculo de la **exactitud (accuracy)** en el conjunto de validación y selección del mejor modelo.
   - Evaluación final en el conjunto de prueba para estimar la calidad real del modelo.

5. **Prueba de cordura (sanity check)**
   - Comparación con un modelo ingenuo (por ejemplo, un clasificador que siempre predice el plan más frecuente).
   - Verificación de que el modelo entrenado realmente aporta valor adicional.

---

**EN 🇬🇧**

The main steps of the project were:

1. **Data loading and inspection**
   - Reading `users_behavior.csv`.
   - Checking data types, missing values, and feature distributions.

2. **Data preparation**
   - Separating features (`calls`, `minutes`, `messages`, `mb_used`) and the target (`is_ultra`).
   - Splitting data into **training**, **validation**, and **test** sets.

3. **Model training**
   - Training several classification models (e.g., decision trees, random forest, logistic regression, etc.).
   - Hyperparameter tuning (tree depth, number of estimators, etc.) using the validation set.

4. **Evaluation**
   - Computing **accuracy** on the validation set and selecting the best model.
   - Final evaluation on the test set to estimate real-world performance.

5. **Sanity check**
   - Comparing against a naive model (e.g., always predicting the most frequent plan).
   - Verifying that the trained model actually adds value.

---

## 🤖 Modelos y resultados / Models and Results

> ⚠️ **Nota / Note:** Sustituye los valores entre corchetes por los resultados reales de tu notebook.

**ES 🇪🇸**

Modelos evaluados (ejemplos):

- Regresión logística  
- Árbol de decisión  
- Bosque aleatorio (Random Forest)  
- (Opcional) Otros modelos de clasificación

El mejor modelo fue:

- **Modelo:** `[Nombre del modelo]`  
- **Hiperparámetros principales:** `[lista de hiperparámetros relevantes]`  
- **Accuracy en validación:** `[accuracy_validación]`  
- **Accuracy en prueba:** `[accuracy_prueba]`  

La **prueba de cordura** mostró que:

- El modelo entrenado supera al modelo ingenuo con una diferencia de accuracy de aproximadamente `[delta_accuracy]`,  
  por lo que resulta útil para recomendar planes a los clientes de Megaline.

---

**EN 🇬🇧**

Models evaluated (examples):

- Logistic Regression  
- Decision Tree  
- Random Forest  
- (Optional) Other classifiers

The best model was:

- **Model:** `[Model name]`  
- **Main hyperparameters:** `[list of relevant hyperparameters]`  
- **Validation accuracy:** `[validation_accuracy]`  
- **Test accuracy:** `[test_accuracy]`  

The **sanity check** showed that:

- The trained model outperforms the naive baseline by about `[delta_accuracy]` in accuracy,  
  so it is useful for recommending the correct plan to Megaline customers.

---

## 📁 Estructura del repositorio / Repository Structure

**ES 🇪🇸**

```text
.
├── Proyecto_10.ipynb      # Notebook principal con todo el análisis y el modelado
├── requirements.txt       # Dependencias del proyecto
└── README.md              # Descripción del proyecto (este archivo)
