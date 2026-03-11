# Documentación del dataset: Advertising Dataset

## a) Nombre de la base de datos
Advertising Dataset

## b) Fuente (URL)
El conjunto de datos es ampliamente utilizado en la literatura de estadística y machine learning. Está disponible en múltiples repositorios, entre ellos:
- [The Elements of Statistical Learning (libro) – datos de publicidad](https://hastie.su.domains/ElemStatLearn/datasets/Advertising.csv)
- [Kaggle: Advertising Dataset](https://www.kaggle.com/datasets/ashydv/advertising-dataset)
- [Statlearning.com – recursos del libro ISLR](https://www.statlearning.com/)

## c) Descripción general del problema
Este conjunto de datos contiene información sobre los presupuestos de publicidad en diferentes medios (TV, radio y periódicos) y las ventas correspondientes de un producto. Cada fila representa una campaña publicitaria o un período de tiempo. El problema típico es de **regresión**, donde se busca modelar la relación entre la inversión publicitaria en cada medio y las ventas generadas, con el fin de predecir ventas futuras o entender la efectividad de cada canal.

## d) Objetivo del análisis
Desarrollar un modelo predictivo que estime las ventas (`Sales`) a partir de los presupuestos asignados a TV, radio y periódicos. Además, se busca identificar qué medio tiene mayor impacto en las ventas y cuantificar la relación, lo que puede ayudar en la toma de decisiones de asignación de presupuesto publicitario.

## e) Variable objetivo (variable respuesta)
`Sales` – Ventas del producto (en miles de unidades, por ejemplo).

## f) Diccionario de variables

| Nombre de la variable | Descripción | Tipo de variable |
|-----------------------|-------------|------------------|
| `TV` | Presupuesto de publicidad en televisión (en miles de dólares) | Numérica continua |
| `Radio` | Presupuesto de publicidad en radio (en miles de dólares) | Numérica continua |
| `Newspaper` | Presupuesto de publicidad en periódicos (en miles de dólares) | Numérica continua |
| `Sales` | Ventas del producto (en miles de unidades) – **variable objetivo** | Numérica continua |

## g) Número de observaciones
El conjunto de datos contiene **200** registros (filas).

## h) Número de variables
El dataset incluye **4** variables (columnas), de las cuales 3 son predictoras y 1 es la variable objetivo.

## i) Posibles hipótesis de estudio

1. **Relación positiva entre inversión en TV y ventas**: Existe una correlación positiva significativa entre el presupuesto de publicidad en televisión y las ventas. Es decir, a mayor inversión en TV, mayores ventas.

2. **Efectividad comparada de los medios**: La publicidad en radio tiene un impacto mayor en las ventas que la publicidad en periódicos, manteniendo constantes las otras variables.

3. **Interacciones entre medios**: Puede existir un efecto de interacción entre la inversión en TV y radio, de modo que la combinación de ambos medios genere un incremento adicional en las ventas más allá de la suma de sus efectos individuales.

4. **Rendimientos decrecientes**: La relación entre la inversión publicitaria y las ventas podría no ser lineal, presentando rendimientos decrecientes a medida que se incrementa el presupuesto en un medio.