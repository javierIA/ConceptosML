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
# KMeans( K-medias)
---
# Introducción
- El algoritmo K-means es un algoritmo de aprendizaje no supervisado que se utiliza para resolver problemas de agrupamiento.

- El agrupamiento es un proceso de agrupación de objetos similares en grupos, denominados clústeres.

---
# Introducción
- El objetivo del algoritmo K-means es encontrar grupos en los datos, con el número de grupos representados por la variable K.

- El algoritmo funciona iterativamente para asignar cada punto de datos a uno de los K grupos en función de las características que se proporcionan.
---

![Alt text](https://i.imgur.com/rwkQNbv.png)

--- 

### 1. Segmentación Conductual

- **Historial de Compras**: Comprender los hábitos de compra de los clientes.
  
    

- **Actividad en la Web**: Agrupar usuarios según patrones de navegación.
  

- **Creación de Personas**: Definir personajes de usuario basados en intereses.


---

### 2. Categorización de Inventario

- **Actividad de Ventas**: Clasificar productos según su desempeño en ventas.


- **Métricas de Fabricación**: Agrupar productos según datos de producción.

---

### 3. Ordenando Mediciones de Sensores

- **Sensores de Movimiento**: Detectar diferentes tipos de actividades físicas.

   

- **Agrupar Imágenes**: Categorizar imágenes similares en clusters.

    

---

### 4. Detección de Bots o Anomalías

- **Actividad Válida vs Bots**: Separar actividades de usuarios genuinos de bots.

    

- **Monitoreo de Salud**: Identificar patrones de salud anormales.

  

---

### Funcionamiento

---

# Funcionamiento del algoritmo KMeans

Vamos a explicar cómo funciona el algoritmo KMeans de la manera más simple posible.

---

# Paso 1: Elegir el número de Clusters 'K'

- 'K' representa el número de clusters que el algoritmo encontrará en el dataset. 
- Elegir el valor correcto de 'K' es muy importante. 
- A veces, 'K' se puede identificar claramente al visualizar el dataset, pero la mayoría de las veces no es así. 

---

# Paso 2: Asignar 'K' puntos aleatorios como centroides

- Estos 'K' puntos pueden ser puntos del dataset o externos. 
- Hay que tener en cuenta que la inicialización aleatoria de los centroides puede causar la "trampa de inicialización aleatoria". 

---

# Paso 3: Asignar puntos del dataset al centroide más cercano

- Cada punto del dataset se asigna al centroide más cercano. 

---

# Paso 4: Calcular el centroide de los clusters individuales

- Se calcula el centroide para cada cluster y se coloca el antiguo centroide allí. 

---

# Paso 5: Reasignar puntos

- Los puntos se reasignan como se hizo en el paso 3. 
- Si hay reasignación, entonces necesitamos volver al paso cuatro. 
- Si no hay reasignación, entonces podemos decir que nuestro modelo ha convergido y está listo.

---

![Alt text](https://i.imgur.com/3jTk7Y0.png)

---
# Elegir el valor correcto de 'K'

---

# Evaluación usando WCSS

- WCSS: Within Cluster Sum of Squares (Suma de Cuadrados dentro del Cluster).
- Debe ser bajo.
- Es una medida de cuán dispersos están los datos dentro de cada cluster.
- Fórmula para K = 3: Suma de Distancia(p,c), que es la suma de las distancias de los puntos en un cluster desde el centroide.

---

# Método del Codo (Elbow Method)

- Se utiliza para elegir el mejor valor de K.
- Se traza WCSS para diferentes valores de K.
- Se busca el "codo" en el gráfico, es decir, el punto después del cual la disminución en WCSS es mínima.
- En el ejemplo dado, después de 3 no hay una disminución significativa en WCSS, por lo que 3 es el mejor valor.

---

![Alt text](https://i.imgur.com/5W63xul.png)

---

![bg](https://i.imgur.com/gi9p7V5.png)

