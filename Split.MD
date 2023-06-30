---
marp: true
theme: gaia
class: lead
backgroundColor: '#2ECC71'
color: '#FFFFFF'
style: |
  section {
    color: #FFFFFF;
    background-color: #2ECC71;
  }
  h1 {
    color: #FFFFFF;
  }
  h2 {
    color: #FFFFFF;
  }
  p {
    color: #FFFFFF;
  }
  .emoji {
    display: inline-block;
    vertical-align: middle;
  }
---

# División de Datos 📚🔍
Uno de los pasos fundamentales en el preprocesamiento de los datos antes de aplicar un algoritmo de aprendizaje automático es dividir los datos en dos conjuntos: el conjunto de entrenamiento y el conjunto de prueba. 🏋️‍♂️🎯

---

# División de Datos 📚🔍
El conjunto de entrenamiento se usa para entrenar nuestro modelo, es decir, para ajustar los parámetros de nuestro algoritmo de aprendizaje automático. El conjunto de prueba se usa para evaluar el rendimiento de nuestro modelo en datos no vistos previamente. 🌍

---

# Razones para la División 🧐
La principal razón para dividir los datos en estos dos conjuntos es evitar el sobreajuste. El sobreajuste ocurre cuando nuestro modelo se ajusta muy bien a los datos de entrenamiento, pero no se desempeña bien en los datos de prueba o en datos nuevos. 😱

---

# Razones para la División 🧐
Al reservar un conjunto de datos para las pruebas, podemos verificar si nuestro modelo es capaz de generalizar bien a datos nuevos.

---

# ¿Cómo Dividir los Datos? 📏
En general, se utiliza una proporción de 70-30 o 80-20 para la división de los datos. Es decir, el 70-80% de los datos se utilizan para el entrenamiento, y el 20-30% restante se utiliza para las pruebas. 

---

# ¿Cómo Dividir los Datos? 📏
Es importante recordar que los datos deben ser divididos de manera aleatoria para evitar cualquier sesgo en el entrenamiento o en las pruebas. En algunos casos, también puede ser útil utilizar una técnica llamada validación cruzada.

---

# Validación Cruzada ⏱
La validación cruzada es una técnica que nos permite usar todos nuestros datos para el entrenamiento y para las pruebas. Dividimos nuestros datos en 'k' partes iguales, o 'folds'.

---

# Validación Cruzada ⏱
Luego, entrenamos nuestro modelo 'k' veces, cada vez usando un 'fold' diferente como nuestro conjunto de prueba y los 'folds' restantes como nuestro conjunto de entrenamiento. 

---

# Validación Cruzada ⏱
Finalmente, promediamos los resultados de estas 'k' pruebas para obtener una medida más robusta de la capacidad de nuestro modelo para generalizar a nuevos datos. La validación cruzada puede ser más costosa en términos de tiempo y recursos computacionales, pero a menudo proporciona una evaluación más precisa de nuestro modelo. 🔄
