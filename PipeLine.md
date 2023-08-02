---
marp: true
theme: default
---

# Pipelines en Scikit-learn

---

# ¿Qué es un Pipeline?

- Un Pipeline agrupa una secuencia de pasos de procesamiento y modelado en un único objeto.
- Cada paso se representa como una tupla, donde el primer elemento es un nombre (string) y el segundo es una instancia de una transformación o un estimador.
- Simplifica el código y previene errores comunes.

---

# Beneficios de usar Pipelines

1. Proporciona una forma sistemática de construir flujos de trabajo.
2. Asegura que se siga el mismo orden de pasos en entrenamiento y evaluación.
3. Simplifica el proceso de ajuste de hiperparámetros.

---

# Creación de un Pipeline Básico: Regresión Lineal

Vamos a ver un ejemplo sencillo utilizando una regresión lineal con escalamiento de características.

---

# Pasos del Pipeline

1. **Escalamiento** de las características usando `StandardScaler`.
2. Entrenamiento de un modelo de **Regresión Lineal**.

---

# Código Básico

```python
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LinearRegression

# Definición del Pipeline
pipeline = Pipeline([
    ('scaler', StandardScaler()),
    ('regressor', LinearRegression())
])

# Entrenamiento
pipeline.fit(X_train, y_train)

# Predicción
y_pred = pipeline.predict(X_test)
