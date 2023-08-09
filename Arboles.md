---
marp: true
theme: default
---

# Árboles de Decisión

---

# Introducción

- Modelo de aprendizaje supervisado.
- Funciona tanto para clasificación como regresión.
- Representa decisiones y sus posibles resultados en forma de árbol.

---

# Estructura de un Árbol de Decisión

- **Nodos**: Representan características o atributos.
- **Ramas**: Representan decisiones.
- **Hojas**: Representan el resultado.

---

# ¿Cómo funciona?

1. Selecciona el mejor atributo usando métricas (Ganancia de Información, Índice Gini).
2. Divide el conjunto de datos según el valor del mejor atributo.
3. Repite el proceso para cada subconjunto hasta que:
    - Todos los datos pertenecen a una misma etiqueta.
    - No quedan atributos.

---

# Métricas de Evaluación de Atributos

## Ganancia de Información

- Basado en el concepto de entropía.
- Selecciona el atributo que proporciona la mayor ganancia de información.

## Índice Gini

- Medida de impureza.
- Un valor menor de Gini indica que un atributo discrimina bien.

---

# Ejemplo en `scikit-learn`

```python
from sklearn.tree import DecisionTreeClassifier

tree = DecisionTreeClassifier(criterion='gini', max_depth=3)
tree.fit(X_train, y_train)
```

---

# Ventajas

1. Fácil de entender e interpretar.
2. Puede manejar tanto datos numéricos como categóricos.
3. Requiere poco preprocesamiento.

---

# Desventajas

1. Sensible a pequeñas variaciones en los datos.
2. Riesgo de sobreajuste.
3. Puede crear árboles complejos que no generalizan bien.

---

# Pruning (Poda)

- Técnica para reducir el tamaño del árbol y prevenir el sobreajuste.
- Elimina secciones del árbol que no aportan poder predictivo.

---

# Importancia de Características

- Los árboles de decisión pueden determinar la importancia de cada característica.
- Muy útil para selección y reducción de características.

---

# Conclusión

- Los árboles de decisión son modelos versátiles y fáciles de interpretar.
- Es fundamental manejarlos adecuadamente para evitar problemas como el sobreajuste.
```

Este es un esquema básico. Puedes personalizarlo y expandirlo según tus necesidades y el contenido que desees cubrir. ¡Espero que te ayude a comenzar!