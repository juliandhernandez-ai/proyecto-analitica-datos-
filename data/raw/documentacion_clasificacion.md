# Documentación del dataset: California Housing Prices

## a) Nombre de la base de datos
California Housing Prices

## b) Fuente (URL)
El conjunto de datos está disponible públicamente en:
- [Kaggle: California Housing Prices](https://www.kaggle.com/datasets/camnugent/california-housing-prices)
- [Scikit-learn: California Housing dataset](https://scikit-learn.org/stable/datasets/real_world.html#california-housing-dataset)

## c) Descripción general del problema
Este conjunto de datos contiene información recopilada a nivel de bloques censales (distritos) en el estado de California durante el año 1990. Cada registro representa un distrito y proporciona variables geográficas, demográficas y habitacionales, así como el valor mediano de las viviendas. El problema típico asociado es la **regresión**, donde se busca predecir el valor mediano de las viviendas (`valormviviendas`) a partir de las demás características disponibles.

## d) Objetivo del análisis
Desarrollar un modelo predictivo que estime el valor mediano de las viviendas en función de variables como la ubicación, el ingreso medio, la edad de las viviendas, el número de habitaciones, la población y la proximidad al océano. Adicionalmente, se busca identificar los factores más influyentes en el precio de la vivienda y comprender las relaciones subyacentes entre las variables.

## e) Variable objetivo (variable respuesta)
`valormviviendas` – Valor mediano de las viviendas en el distrito (expresado en dólares estadounidenses).

## f) Diccionario de variables

| Nombre de la variable | Descripción | Tipo de variable |
|-----------------------|-------------|------------------|
| `longitud` | Coordenada geográfica de longitud del centro del bloque censal | Numérica continua |
| `latitud` | Coordenada geográfica de latitud del centro del bloque censal | Numérica continua |
| `edadmc` | Edad mediana de las viviendas (antigüedad en años) | Numérica discreta |
| `totalhabitaciones` | Número total de habitaciones en el distrito | Numérica discreta |
| `totaldormitorios` | Número total de dormitorios en el distrito | Numérica discreta |
| `poblacion` | Población total del distrito | Numérica discreta |
| `hogares` | Número total de hogares en el distrito | Numérica discreta |
| `ingresomedio` | Ingreso medio de los hogares (en decenas de miles de dólares) | Numérica continua |
| `valormviviendas` | Valor mediano de las viviendas (dólares) – **variable objetivo** | Numérica continua |
| `ocean_proximity` | Proximidad al océano (categoría codificada numéricamente) | Categórica nominal |

> **Nota:** En el archivo original, la variable `ocean_proximity` aparece con valores numéricos (1.0, 3.0, etc.) que corresponden a categorías como "<1H OCEAN", "INLAND", "NEAR OCEAN", "NEAR BAY", "ISLAND". Para fines de análisis, debe tratarse como categórica nominal.

## g) Número de observaciones
El conjunto de datos contiene **20.640** registros (filas), correspondientes a otros tantos bloques censales.

## h) Número de variables
El dataset incluye **10** variables (columnas), de las cuales 9 son predictores y 1 es la variable objetivo.

## i) Posibles hipótesis de estudio

1. **Relación entre ingreso y valor de vivienda**: Existe una correlación positiva significativa entre el ingreso medio de los hogares (`ingresomedio`) y el valor mediano de las viviendas (`valormviviendas`). Es decir, a mayor ingreso, mayor precio de la vivienda.

2. **Influencia de la ubicación geográfica**: Las viviendas situadas más cerca de la costa (menor distancia al océano, según la categoría `ocean_proximity`) tienen un valor mediano superior al de aquellas ubicadas en el interior.

3. **Impacto del tamaño de la vivienda**: El número de habitaciones (`totalhabitaciones`) y dormitorios (`totaldormitorios`) está positivamente asociado con el valor de la vivienda, aunque esta relación puede estar mediada por el número de hogares y la densidad poblacional.

4. **Efecto de la antigüedad**: Las viviendas más nuevas (menor `edadmc`) tienden a tener un valor más alto, aunque esta relación podría no ser lineal debido a la posible renovación de propiedades antiguas en zonas de alta demanda.