---
marp: true
theme: gaia
style: |
  section {
    background-color: #ECF0F1;
    color: #2C3E50;
  }
  h1, h2, h3 {
    color: #16A085;
  }
---

# Métricas de Evaluación de Modelos 📏

Cuando entrenamos modelos de machine learning, es esencial tener maneras de evaluar su rendimiento. Para las tareas de clasificación, algunas de las métricas más comunes incluyen la precisión (accuracy), la matriz de confusión, la precisión (precision), la exhaustividad (recall) y la puntuación F1.

---

# Accuracy (Precisión) 🎯

La precisión es la fracción de predicciones que el modelo acertó.

`Accuracy = (TP + TN) / (TP + TN + FP + FN)`

Donde:

- TP = Verdaderos Positivos
- TN = Verdaderos Negativos
- FP = Falsos Positivos
- FN = Falsos Negativos

---

# Matriz de Confusión 🧮

La matriz de confusión es una tabla que se usa para describir el rendimiento de un modelo de clasificación en un conjunto de datos para los cuales se conocen los valores verdaderos.

- **Verdaderos Positivos (TP)**: Los casos en los que el modelo predijo correctamente la clase positiva.
- **Verdaderos Negativos (TN)**: Los casos en los que el modelo predijo correctamente la clase negativa.
- **Falsos Positivos (FP)**: Los casos en los que el modelo predijo incorrectamente la clase positiva.
- **Falsos Negativos (FN)**: Los casos en los que el modelo predijo incorrectamente la clase negativa.
---
![bg 70% ](https://miro.medium.com/max/712/1*Z54JgbS4DUwWSknhDCvNTQ.png)

---

# Precision y Recall ⚖️

- **Precision (Precisión)**: La precisión es la fracción de predicciones correctas entre las instancias que el modelo predijo como positivas. 
`Precision = TP / (TP + FP)`

- **Recall (Exhaustividad o sensibilidad)**: La exhaustividad es la fracción de instancias positivas que el modelo predijo correctamente. 
`Recall = TP / (TP + FN)`

---

# F1 Score 🥇

El F1 Score es una medida que combina la precisión y la exhaustividad. Es la media armónica de ambas medidas, y da un valor más alto si ambas medidas son similares.

`F1 = 2 * (Precision * Recall) / (Precision + Recall)`

---
# Error Cuadrático Medio (MSE)


Descripción del Error Cuadrático Medio
El Error Cuadrático Medio (MSE) es una métrica común para evaluar modelos de regresión. Mide el promedio de los cuadrados de los errores, es decir, la diferencia cuadrada media entre los valores estimados y los valores reales.


---

# Ejemplo de Evaluación de un Modelo de Clasificación 🧪

- Vamos a asumir que hemos entrenado un modelo para predecir si un email es spam (la clase positiva) o no (la clase negativa). En nuestro conjunto de prueba de 1000 correos electrónicos, el modelo hizo las siguientes predicciones:
---
# Ejemplo de Evaluación de un Modelo de Clasificación 🧪
- Verdaderos Positivos (TP): 200 (El modelo correctamente identificó 200 correos electrónicos como spam)
- Verdaderos Negativos (TN): 600 (El modelo correctamente identificó 600 correos electrónicos como no spam)
- Falsos Positivos (FP): 50 (El modelo incorrectamente identificó 50 correos electrónicos como spam)
- Falsos Negativos (FN): 150 (El modelo incorrectamente identificó 150 correos electrónicos como no spam)
Accuracy (Precisión) 🎯
---
Vamos a calcular la precisión de nuestro modelo usando la fórmula: Accuracy = (TP + TN) / (TP + TN + FP + FN)

Accuracy = (200 + 600) / (200 + 600 + 50 + 150) = 800 / 1000 = 0.8 or 80%

# Nuestro modelo tiene una precisión del 80%.
---
# Matriz de Confusión 🧮
Aquí está la matriz de confusión de nuestro modelo:

-	Predicción Positiva	Predicción Negativa
- Positiva Verdadera	200 (TP)	150 (FN)
- Negativa Verdadera	50 (FP)	600 (TN)
---
# Precision y Recall ⚖️
- Vamos a calcular la precisión y la exhaustividad de nuestro modelo:

- Precision (Precisión): Precision = TP / (TP + FP) = 200 / (200 + 50) = 0.8 or 80%
- Recall (Exhaustividad o sensibilidad): Recall = TP / (TP + FN) = 200 / (200 + 150) = 0.57 or 57%
---
# F1 Score 🥇
Finalmente, calculamos el F1 Score de nuestro modelo usando la fórmula: F1 = 2 * (Precision * Recall) / (Precision + Recall)

F1 = 2 * (0.8 * 0.57) / (0.8 + 0.57) = 0.67 or 67%

