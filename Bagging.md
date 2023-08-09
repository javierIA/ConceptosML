---
marp: true
theme: default
---

# Metaclasificadores y Metaregresores con Bagging

---

# Introducción

- **Meta-algoritmos** extienden y combinan modelos base para mejorar el rendimiento.
- **Bagging** (Bootstrap Aggregating) es una técnica de ensamble que reduce la varianza y previene el sobreajuste.

---

# ¿Qué es Bagging?

- Técnica que utiliza subconjuntos de datos (bootsrap samples) para entrenar múltiples instancias del modelo.
- Las predicciones se realizan mediante voto mayoritario (para clasificación) o promedio (para regresión).

---

# Metaclasificadores

- Extienden la funcionalidad de los clasificadores base.
- Ejemplo: `BaggingClassifier` en `scikit-learn`.

---

# Metaclasificador: BaggingClassifier

```python
from sklearn.ensemble import BaggingClassifier
from sklearn.tree import DecisionTreeClassifier

tree = DecisionTreeClassifier()
bagging = BaggingClassifier(base_estimator=tree, n_estimators=100, random_state=0)
bagging.fit(X_train, y_train)
```

---

# Metaregresores

- Similar a los metaclasificadores, pero para tareas de regresión.
- Ejemplo: `BaggingRegressor` en `scikit-learn`.

---

# Metaregresor: BaggingRegressor

```python
from sklearn.ensemble import BaggingRegressor
from sklearn.tree import DecisionTreeRegressor

tree_reg = DecisionTreeRegressor()
bagging_reg = BaggingRegressor(base_estimator=tree_reg, n_estimators=100, random_state=0)
bagging_reg.fit(X_train, y_train)
```

---

# Beneficios del Bagging

1. Reducción del sobreajuste.
2. Mejora en la estabilidad y precisión del modelo.
3. Capacidades de paralelización al entrenar y predecir.
4. Manejo de datos faltantes.

---

# Desventajas del Bagging

1. Mayor consumo de recursos computacionales.
2. Pérdida de interpretabilidad.

---

# Conclusión

- Los metaclasificadores y metaregresores con bagging proporcionan una herramienta poderosa para mejorar el rendimiento del modelo.
- Aunque consumen más recursos, los beneficios en términos de precisión y robustez pueden justificar su uso en muchos escenarios.
```

Puedes expandir o personalizar estos slides según tus necesidades y el contenido que quieras abordar. Esta estructura es solo un punto de partida que te da una idea general del tema. ¡Espero que te sea útil!