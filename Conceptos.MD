---
marp: true
theme: gaia
author: Javier Flores 
style: |
  h1 {
    color: #00FF00;
  }
  p {
    color: #00FF00;
  }
  section {
    background-color: #000000;
  }
  section.lead {
    background-color: #000000;
  }
  section.lead h1 {
    color: #00FF00;
  }
  section.lead p {
    color: #00FF00;
  }
backgroundColor: #000000
footer: "Introducción al Machine Learning"
jpegQuality: 100
paginate: true
description: "Introducción al Machine Learning"
color: #FFFFFF



---

# Introducción al Machine Learning
### Definición, Tipos y Aplicaciones

---

# ¿Qué es Machine Learning?
- Disciplina de la inteligencia artificial.
- Genera sistemas capaces de aprender a través de la "experiencia".
- No se desarrolla explícitamente la lógica, se proporcionan datos y resultados esperados para entrenar un algoritmo.

---

# Definición Formal de Machine Learning
- "Un programa se dice que aprende a través de la experiencia con respecto a un tipo de tareas y una medición de su desempeño, si su desempeño en las tareas, medidas por, mejora a través de la experiencia E." - Mitchell 1997

---

# Programación Tradicional vs Machine Learning
- Programación Tradicional: El desarrollador escribe las reglas y las instrucciones.
- Machine Learning: El algoritmo aprende las reglas e instrucciones de los datos proporcionados.

---

# Ejemplo: Perros vs Gatos
- En la programación tradicional, un desarrollador tendría que escribir todas las posibles características de un perro y un gato para diferenciarlos.
- En el machine learning, el algoritmo aprende a diferenciar un perro de un gato basándose en un conjunto de imágenes etiquetadas de perros y gatos.

---

# Tipos de Algoritmos de Machine Learning (1/2)
- Supervisado: El algoritmo aprende a través de ejemplos previamente clasificados.
- No Supervisado: El algoritmo aprende a través de ejemplos sin clasificar y descubre patrones por sí mismo.

---

# Tipos de Algoritmos de Machine Learning (2/2)
- Reforzado: El algoritmo aprende a través de la experiencia, recibe recompensas que le indican si las acciones realizadas han sido correctas o no.

---

# Problemas que Resuelve el Machine Learning (1/2)
- Clasificación: Asignar una etiqueta a un ejemplo sin clasificar (detección de spam).
- Regresión: Predecir un valor dado un ejemplo sin etiquetar (precio de una casa).

---

# Problemas que Resuelve el Machine Learning (2/2)
- Asociación: Relacionar instancias con características similares (noticias similares).
- Agrupación (Clustering): Agrupar los datos de tal forma que los elementos de estos grupos sean similares (segmentación de clientes).

---

# ¿Hemos utilizado ya Machine Learning?
- En el tema de "Sistemas clasificadores (Learning classifier system)", realizamos algoritmos de machine learning de categorías de aprendizaje supervisado y reforzado.

---

# Importancia del Machine Learning (1/2)
- Nos permite resolver tareas que de otra manera serían prácticamente imposibles.
- Ha sido aplicado en una variedad de ámbitos de manera exitosa.

---

# Importancia del Machine Learning (2/2)
- Aplicaciones en diversos campos: Procesamiento del lenguaje natural, Visión por computadora, Detección de amenazas, Evaluación de clientes, Sistemas de recomendación, Detección de anomalías, Reconocimiento de genes en secuencias de ADN, y más.

---

# Introducción al Aprendizaje Supervisado
- Aquí revisaremos varios algoritmos de machine learning que utilizan aprendizaje supervisado.
- Para esto, primero observaremos algunas generalidades presentes en este tipo de aprendizaje.

---

# Recolección de Datos
- El proceso suele iniciar con la recolección de los datos.
- Estos datos conforman nuestro conjunto de datos (dataset), compuesto de una serie de pares de datos (entrada, salida).

---

# Transformación de Datos
- Los datos de entrada suelen estar compuestos de un vector de atributos.
- Es deber del analista de datos determinar cómo convertir una entidad del mundo real a un vector de atributos y cómo transformar o extraer las características relevantes del problema.

---

# Tipos de Datos (1/2)
- Datos numéricos: Números continuos o discretos.
- Datos ordinales: Variables en categorías ordenadas, la distancia entre dos categorías no se establece.

---

# Tipos de Datos (2/2)
- Datos categóricos: Variables en categorías no ordenadas.

---

# Conclusión
- El Machine Learning es una herramienta poderosa que permite a las computadoras aprender de los datos y mejorar su desempeño en tareas específicas.
- Dependiendo del problema y los datos disponibles, se pueden utilizar diferentes tipos de algoritmos de machine learning.
- El machine learning tiene una amplia gama de aplicaciones en diversas disciplinas y campos, lo que resalta su importancia y potencial en la era actual de los datos.

---

# Gracias por su atención!
- ¿Preguntas?

---
#