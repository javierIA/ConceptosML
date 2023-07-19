---
marp: true
theme: gaia
class: lead
style: |
  section {
    background-color: #D6EAF8;
  }
  h1, h2, h3 {
    color: #154360;
  }
  p {
    color: #154360;
  }
---

# Introducción a K-Nearest Neighbors (KNN)

---

# ¿Qué es KNN?

K-Nearest Neighbors (KNN) es un algoritmo de aprendizaje supervisado que se puede utilizar tanto para problemas de clasificación como de regresión. La idea principal de KNN es que los puntos de datos similares deben tener la misma etiqueta.

---

# ¿Cómo funciona KNN?

1. Cuando un nuevo punto de datos llega, el algoritmo KNN busca los K puntos más cercanos al nuevo punto de datos en el conjunto de entrenamiento. 

2. Entonces, según el problema:
    - **Regresión**: Toma el promedio de las etiquetas de estos K puntos para predecir la etiqueta del nuevo punto de datos.
    - **Clasificación**: Toma el voto mayoritario de las etiquetas de estos K puntos para predecir la etiqueta del nuevo punto de datos.

---

![bg = 60% ](https://miro.medium.com/v2/resize:fit:720/0*Rxd_UYjOPrK7_gk4)

---
# Medida de distancia en KNN

La similitud entre los puntos se mide a menudo utilizando medidas de distancia, como la distancia euclídea, la distancia Manhattan, la distancia Minkowski, entre otras. 

---

# Eligiendo el valor de K

El valor de K tiene un gran impacto en los resultados de KNN. Un K muy pequeño puede hacer que el modelo sea sensible al ruido y a los outliers, mientras que un K muy grande puede hacer que el modelo sea demasiado general.

---

![bg = 80% ](https://miro.medium.com/v2/resize:fit:720/0*kh-nHGVTxrpvVsjj)

---

# Ventajas de KNN

- Simple de entender y fácil de implementar.
- No asume ninguna suposición sobre los datos.
- Se adapta fácilmente a los datos multiclase.

---

# Desventajas de KNN

- La elección de K puede ser complicada.
- Es sensible a las características irrelevantes y a la escala de los datos.
- El tiempo de cálculo puede ser alto para conjuntos de datos grandes.


---


# KNN para principiantes

---

# ¿Qué es KNN?

KNN, o k-nearest neighbors, es un algoritmo simple que predice la etiqueta de un punto basado en las etiquetas de los 'k' puntos más cercanos.

![bg = 60% ](https://live.staticflickr.com/65535/47646856032_e693b87caa_b.jpg)

---

# ¿Cómo funciona KNN?

Imagina que estás en un partido de fútbol, pero no sabes a qué equipo apoya cada fan. Decides que el equipo que apoya un fan es probablemente el mismo equipo que los fans más cercanos a él apoyan.

---

# ¿Cómo se calcula "más cercano"?

La "cercanía" se calcula usando la "distancia". Cuanto menor sea la distancia entre dos puntos, más "cercanos" se consideran. Hay varias formas de calcular la distancia, pero las más comunes son la distancia euclídea (la línea recta entre dos puntos) y la distancia de Manhattan (como si caminaras por las calles de una ciudad).

![Distancias](https://live.staticflickr.com/65535/40733598823_0eede41717_b.jpg)

---

# ¿Qué significa 'k'?

'k' es el número de vecinos que se toman en cuenta. Por ejemplo, si k=3, se miran los 3 fans más cercanos para decidir a qué equipo probablemente apoya un fan.

![Vecinos](https://miro.medium.com/max/1200/1*OAm4kCJ_jVI-6xQ5M3EEVg.png)

---

# ¿Cómo elegimos 'k'?

El valor de 'k' a menudo se elige mediante ensayo y error. Si k es demasiado pequeño, el modelo puede ser demasiado sensible a los puntos de datos individuales (sobreajuste). Si k es demasiado grande, el modelo puede ser demasiado general (subajuste).

---

# ¿Y si las características están en diferentes escalas?

Es importante que todas las características tengan la misma escala cuando se calculan las distancias. Por ejemplo, si estás midiendo la altura en centímetros y el peso en kilogramos, un pequeño cambio en el peso resultará en una gran distancia. Para evitar esto, a menudo se "normalizan" las características para que todas estén en la misma escala.

![Normalización](https://miro.medium.com/max/1190/1*_783tuRRdY9UJU1wIgaMwA.png)

---

# ¿KNN es para clasificación o regresión?

¡Ambos! Para la clasificación, la etiqueta es la más común entre los k vecinos (por ejemplo, si k=3 y las etiquetas son [Perro, Perro, Gato], la etiqueta será Perro). Para la regresión, la etiqueta es el promedio de las etiquetas de los k vecinos.

![Clasificación y Regresión](https://miro.medium.com/max/1400/1*7J08ekAwupLBegeUI8muHA.png)

