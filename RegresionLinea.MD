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
footer: "Regresión Lineal Simple"
jpegQuality: 100
paginate: true
description: "Regresión Lineal Simple"
color: #ffffff
---

# Regresión Lineal Simple
- Técnica estadística para modelar la relación entre una variable dependiente y una variable independiente.
- Ecuación: Y = a + bX + ε


---

# Variables en la Ecuación
- Y: Variable dependiente
- X: Variable independiente
- a: Intercepción en Y
- b: Pendiente de la línea
- ε: Error (variación no explicada)

- Pendiente = b = Σ [(xi - x̄) * (yi - ȳ)] / Σ [(xi - x̄)²]
---

# Estimación de los Parámetros
- Se usa el método de los mínimos cuadrados para minimizar la suma de los cuadrados de los residuales (errores).

---

# Uso de la Regresión Lineal Simple
- Predicción de valores de Y basados en X
- Evaluación de la fuerza de la relación entre las variables
- Evaluación de la dirección de la relación (positiva/negativa)
### Ejemplo: Predicción de ventas de un producto basado en el gasto en publicidad.


---
![bg ](https://aprendeia.com/wp-content/uploads/2018/11/48051791826_299fb750ea_o-1536x897.png)

--- 
Google Colab






| Gasto en Publicidad (X) | Ventas (Y) |
|---------------------|--------|
| 1000                | 200    |
| 1500                | 300    |
| 1800                | 350    |
| 1200                | 250    |
| 1600                | 320    |
| 2000                | 410    |
| 2200                | 420    |


--- 
En este conjunto de datos, X representa el gasto en publicidad y Y las ventas correspondientes. La idea es que a medida que aumenta el gasto en publicidad, también lo hacen las ventas del producto, por lo que esperamos ver una relación positiva.

Con este conjunto de datos, puedes seguir adelante y aplicar las operaciones de regresión lineal simple que describí en mi mensaje anterior para calcular la pendiente de la línea que mejor se ajusta a estos datos. Esta línea te permitirá predecir el efecto que tendría un cambio en el gasto de publicidad en las ventas del producto.
