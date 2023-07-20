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

# Escalamiento, Normalización y Estandarización de Datos

---

# Introducción

- Los algoritmos de Machine Learning son sensibles a la escala de los datos.
- Datos en diferentes escalas pueden afectar el rendimiento del algoritmo.
- La normalización y la estandarización son técnicas para resolver este problema.

---

# Escalamiento

El escalamiento cambia el rango de los datos para que todos estén en la misma escala, como [0,1] o [-1,1].

**Ejemplo**: Convertir un rango de salarios de 20,000 a 100,000 a un rango de 0 a 1.

---

# Normalización

Transforma las características para que tengan una magnitud de norma unitaria. 

Fórmula:
\[ X_{norm} = \frac{X - X_{min}}{X_{max} - X_{min}} \]

---

# Estandarización

Transforma las características para que tengan una media de 0 y una desviación estándar de 1.

Fórmula:
\[ X_{std} = \frac{X - \mu}{\sigma} \]

Donde:
- \( \mu \) es la media
- \( \sigma \) es la desviación estándar

---

# Usando Python para Escalar Datos

Usaremos `scikit-learn`, una de las bibliotecas más populares para Machine Learning.

```python
from sklearn.preprocessing import MinMaxScaler, StandardScaler

# Datos
data = [[-1, 2], [-0.5, 6], [0, 10], [1, 18]]

# Escalador Min-Max (Normalización)
scaler = MinMaxScaler()
print(scaler.fit_transform(data))

# Estandarizador
scaler = StandardScaler()
print(scaler.fit_transform(data))
```

---

# ¿Cuándo usar qué?

- **Normalización**: Útil cuando no sabes la distribución de tus datos o cuando sabes que la distribución no es Gaussiana.
  
- **Estandarización**: Útil cuando los datos tienen una distribución Gaussiana.

---

# Ventajas y Desventajas

**Ventajas:**
- Mejora el rendimiento de muchos algoritmos.
- Proceso rápido y fácil de implementar.

**Desventajas:**
- La pérdida de interpretabilidad.
- No siempre es necesario (depende del algoritmo).

---

# Resumen

- Escalar tus datos es un paso crucial en el preprocesamiento de datos para Machine Learning.
- `scikit-learn` ofrece herramientas fáciles de usar para normalizar y estandarizar tus datos.
- Elige la técnica adecuada según la distribución de tus datos y el algoritmo que planeas usar.

Ahora estás listo para preparar tus datos para Machine Learning en Python de manera más efectiva!