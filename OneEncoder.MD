---
marp: true
theme: gaia
class: lead
style: |
    :root {
        --primary-bg: #FFD166; /* fondo amarillo pastel */
        --secondary-bg: #06D6A0; /* verde menta */
        --primary-text: #2C3E50; /* azul oscuro */
        --secondary-text: #FF6B6B; /* rojo melocotón */
    }
    section {
    background-color: var(--primary-bg);
    color: var(--primary-text);
    border: 5px solid var(--secondary-bg);
    }
    h1, h2, h3 {
        color: var(--secondary-text);
        border-bottom: 2px solid var(--secondary-bg);
        padding-bottom: 10px;
    }
    p {
        color: var(--secondary-text);
    text-decoration: underline;
    }
    ul, ol {
    color: var(--primary-text);
    }
    blockquote {
    border-left: 5px solid var(--secondary-bg);
    padding-left: 10px;
    color: var(--secondary-text);
    }
    img {
    border: 5px solid var(--secondary-bg);
    }
    table {
    border-collapse: collapse;
    }
---

# Codificación de Datos Categóricos Nominales

---

# ¿Qué son los datos categóricos nominales?

Los datos categóricos son aquellos que representan categorías. Los nominales son aquellos que no tienen un orden específico. Por ejemplo:

- Colores: Rojo, Azul, Verde
- Marcas de autos: Toyota, BMW, Ford


---

# ¿Por qué necesitamos codificarlos?

Los modelos de Machine Learning trabajan con números, no con palabras. Por lo tanto, necesitamos convertir nuestras categorías en una forma numérica.

---

# One Hot Encoding

El enfoque más común es "One Hot Encoding". Crea una columna para cada categoría y utiliza 0s y 1s para representar la presencia de esa categoría.

![One Hot Encoding](https://i.imgur.com/mtimFxh.png)

---

# Codificación con Python

Usaremos `pandas`, una biblioteca popular en Python para manipulación de datos.

```python
import pandas as pd

# Crear un DataFrame de ejemplo
df = pd.DataFrame({
    'color': ['rojo', 'azul', 'verde', 'rojo']
})

# Aplicar One Hot Encoding
encoded_df = pd.get_dummies(df, columns=['color'])
```

---

# Resultado

El DataFrame codificado se verá así:

```
   color_azul  color_rojo  color_verde
0          0           1            0
1          1           0            0
2          0           0            1
3          0           1            0
```

---

# Ventajas y Desventajas

**Ventajas:**

- Fácil de implementar.
- Funciona bien con la mayoría de los algoritmos.

**Desventajas:**

- Aumenta la dimensionalidad de los datos, lo que puede hacer que algunos algoritmos sean más lentos.
- No captura ninguna información sobre la relación entre las categorías.

---

# Resumen

- Los datos categóricos nominales necesitan ser codificados para ser utilizados en modelos de Machine Learning.
- One Hot Encoding es un enfoque común para hacerlo en Python utilizando `pandas`.
- Es importante ser consciente de la dimensionalidad añadida y considerar otras técnicas si es necesario.

¡Ahora estás listo para codificar datos categóricos y utilizarlos en tus modelos de Machine Learning!