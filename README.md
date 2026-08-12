# customer-similarity-knn-insurance
kNN-based customer similarity search and conversion-propensity classifier for an insurance company, with a from-scratch linear regression and a mathematical proof for privacy-preserving data obfuscation (F1=0.92 vs. 0.21 baseline).

## English

### Problem
Sure Tomorrow, an insurance company, wants to explore whether machine learning can solve four business tasks: finding customers similar to a given one (for targeted marketing), predicting whether a new customer is likely to receive an insurance benefit, predicting the number of benefits a customer will receive, and protecting customers' personal data without degrading model performance.

### Approach
- **Task 1 — Similar customers:** implemented a k-Nearest Neighbors search (`NearestNeighbors`) to find customers with similar profiles, comparing scaled vs. unscaled data and different distance metrics (Euclidean, Manhattan).
- **Task 2 — Benefit classification:** built a kNN classifier to predict whether a customer will receive a benefit, comparing its performance against a dummy baseline.
- **Task 3 — Benefit regression:** implemented linear regression from scratch using the normal equation, and validated that feature scaling does not affect its RMSE — unlike kNN.
- **Task 4 — Data obfuscation:** proved analytically (and validated computationally) that multiplying the feature matrix by a random invertible matrix protects personal data without changing the linear regression's predictions or RMSE.

### Results
- Similarity search confirmed that scaling is critical: unscaled data lets high-magnitude features (income) dominate the distance calculation.
- Classification: **F1 = 0.92** (scaled data, k=1) vs. **F1 = 0.21** for the best dummy model.
- Regression: **RMSE = 0.36**, unchanged after data obfuscation — confirming both mathematically and empirically that privacy protection came at no cost to model quality.

### Stack
Python | pandas | scikit-learn | NumPy | Jupyter Notebook

---

## Español

### Problema
Sure Tomorrow, una aseguradora, quiere explorar si el machine learning puede resolver cuatro tareas de negocio: encontrar clientes similares a uno dado (para marketing dirigido), predecir si un nuevo cliente recibirá un beneficio de seguro, predecir la cantidad de beneficios que recibirá, y proteger los datos personales de los clientes sin degradar el desempeño del modelo.

### Enfoque
- **Tarea 1 — Clientes similares:** se implementó una búsqueda de k vecinos más cercanos (`NearestNeighbors`) para encontrar clientes con perfiles similares, comparando datos escalados vs. sin escalar y distintas métricas de distancia (euclidiana, Manhattan).
- **Tarea 2 — Clasificación de beneficio:** se construyó un clasificador kNN para predecir si un cliente recibirá un beneficio, comparando su desempeño contra un modelo dummy de referencia.
- **Tarea 3 — Regresión de beneficios:** se implementó regresión lineal desde cero usando la ecuación normal, y se validó que el escalado de features no afecta su RECM — a diferencia de kNN.
- **Tarea 4 — Ofuscación de datos:** se demostró analíticamente (y se validó computacionalmente) que multiplicar la matriz de características por una matriz invertible aleatoria protege los datos personales sin cambiar las predicciones ni la RECM de la regresión lineal.

### Resultados
- La búsqueda de similitud confirmó que el escalado es crítico: sin escalar, las features de mayor magnitud (ingreso) dominan el cálculo de distancia.
- Clasificación: **F1 = 0.92** (datos escalados, k=1) vs. **F1 = 0.21** del mejor modelo dummy.
- Regresión: **RECM = 0.36**, sin cambios tras la ofuscación de datos — confirmando tanto matemática como empíricamente que la protección de privacidad no tuvo costo en la calidad del modelo.

### Stack
Python | pandas | scikit-learn | NumPy | Jupyter Notebook

---

**Santiago Quintanilla** — Mechatronics Engineer | Data Science Student @ TripleTen
LinkedIn: https://www.linkedin.com/in/santiago-quintanilla-zurita
GitHub: https://github.com/borre3205
