---
marp: true
class: center, middle
theme: gaia
paginate: true
backgroundColor: #2d2d2d
style: |
  h1, h2, h3, h4, h5 {
    color: #b2f3e1;
  }
  p, li {
    color: #d2d2d2;
  }
  code {---
marp: true
class: center, middle
theme: gaia
paginate: true
backgroundColor: #2d2d2d
style: |
  h1, h2, h3, h4, h5 {
    color: #b2f3e1;
  }
  p, li {
    color: #d2d2d2;
  }
  code {
    color: #db7070;
  }

---

# Regresión Ridge y Lasso

---

# Regresión Ridge
La regresión Ridge es una técnica para analizar múltiples variables de regresión cuando hay multicolinealidad (relaciones entre las variables predictoras).

---

# Función de Coste en Regresión Ridge
![](https://latex.codecogs.com/gif.latex?J%28%5Ctheta%29%20%3D%20MSE%28%5Ctheta%29%20%2B%20%5Calpha%20%5Csum_%7Bj%3D1%7D%5En%20%5Ctheta_j%5E2)

Donde $\alpha$ es el parámetro de regularización que controla la cantidad de contracción: cuanto mayor sea $\alpha$, más pequeños serán los coeficientes y mayor será la regularización.

---

# ¿Por qué Regresión Ridge?
La regresión Ridge es una excelente herramienta para utilizar cuando tenemos multicolinealidad o cuando queremos prevenir el overfitting.

---

# Regresión Lasso
Lasso es un método de regresión que realiza regularización y selección de características para mejorar la precisión y la interpretabilidad del modelo de regresión.

---

# Función de Coste en Regresión Lasso
![](https://latex.codecogs.com/gif.latex?J%28%5Ctheta%29%20%3D%20MSE%28%5Ctheta%29%20%2B%20%5Calpha%20%5Csum_%7Bj%3D1%7D%5En%20%7C%5Ctheta_j%7C)

Aquí también, $\alpha$ es el parámetro de regularización. Sin embargo, a diferencia de la regresión Ridge, Lasso puede hacer que algunos coeficientes se reduzcan a cero, eliminando así algunas características.

---

# ¿Por qué Regresión Lasso?
Lasso es especialmente útil cuando se tiene un gran número de características y se espera que solo algunas de ellas sean importantes. Lasso puede ayudar a seleccionar las características más útiles.

---

# Comparación: Ridge vs Lasso
Ridge es una buena opción cuando todas las variables son importantes, mientras que Lasso es una mejor opción cuando solo algunas variables son importantes.

---

# En resumen
Ambos métodos son formas poderosas de regularización que pueden ser muy útiles en situaciones de multicolinealidad y cuando se quiere prevenir el overfitting. Es importante elegir el método correcto según el contexto y los datos disponibles.
    color: #db7070;
  }

---

# Regresión Ridge y Lasso

---

# Regresión Ridge
La regresión Ridge es una técnica para analizar múltiples variables de regresión cuando hay multicolinealidad (relaciones entre las variables predictoras).

---

# Función de Coste en Regresión Ridge
![](https://latex.codecogs.com/gif.latex?J%28%5Ctheta%29%20%3D%20MSE%28%5Ctheta%29%20%2B%20%5Calpha%20%5Csum_%7Bj%3D1%7D%5En%20%5Ctheta_j%5E2)

Donde $\alpha$ es el parámetro de regularización que controla la cantidad de contracción: cuanto mayor sea $\alpha$, más pequeños serán los coeficientes y mayor será la regularización.

---

# ¿Por qué Regresión Ridge?
La regresión Ridge es una excelente herramienta para utilizar cuando tenemos multicolinealidad o cuando queremos prevenir el overfitting.

---

# Regresión Lasso
Lasso es un método de regresión que realiza regularización y selección de características para mejorar la precisión y la interpretabilidad del modelo de regresión.

---

# Función de Coste en Regresión Lasso
![](https://latex.codecogs.com/gif.latex?J%28%5Ctheta%29%20%3D%20MSE%28%5Ctheta%29%20%2B%20%5Calpha%20%5Csum_%7Bj%3D1%7D%5En%20%7C%5Ctheta_j%7C)

Aquí también, $\alpha$ es el parámetro de regularización. Sin embargo, a diferencia de la regresión Ridge, Lasso puede hacer que algunos coeficientes se reduzcan a cero, eliminando así algunas características.

---

# ¿Por qué Regresión Lasso?
Lasso es especialmente útil cuando se tiene un gran número de características y se espera que solo algunas de ellas sean importantes. Lasso puede ayudar a seleccionar las características más útiles.

---

# Comparación: Ridge vs Lasso
Ridge es una buena opción cuando todas las variables son importantes, mientras que Lasso es una mejor opción cuando solo algunas variables son importantes.

---

# En resumen
Ambos métodos son formas poderosas de regularización que pueden ser muy útiles en situaciones de multicolinealidad y cuando se quiere prevenir el overfitting. Es importante elegir el método correcto según el contexto y los datos disponibles.

---

# Ridge Regression

Ridge Regression es una técnica usada para analizar datos de regresión múltiple que sufren de multicolinealidad. 

---

![ridge_formula](https://miro.medium.com/max/644/1*Jd03Hyt2bpEv1r7UijLlpg.png)

donde:

- Y es la variable dependiente.
- X representa la matriz de datos (cada columna es un conjunto de datos predictores).
- β es el vector de coeficientes de regresión.
- n es el número de observaciones.
- p es el número de predictores.
- λ es el parámetro de penalización.

---

# Lasso Regression

Lasso Regression (Least Absolute Shrinkage and Selection Operator) es un tipo de regresión lineal que utiliza contracción. Lasso puede forzar la magnitud de los coeficientes de algunas variables a ser exactamente cero.

---

![lasso_formula](https://miro.medium.com/max/644/1*Jd03Hyt2bpEv1r7UijLlpg.png)

donde:

- Y es la variable dependiente.
- X representa la matriz de datos (cada columna es un conjunto de datos predictores).
- β es el vector de coeficientes de regresión.
- n es el número de observaciones.
- p es el número de predictores.
- λ es el parámetro de penalización.

---

En ambos casos, el término adicional (penalización) hace que los coeficientes de las características correlacionadas se reduzcan, ayudando a resolver el problema de la multicolinealidad y también en la selección de características (en el caso de Lasso).

---