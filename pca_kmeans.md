# Ejercicio

## Importación, carga y exploración inicial

- Descargue los siguientes datos y léalos en Google Colab.
- Cargue las librerías necesarias para el ejercicio: `sklearn`, `pandas`, `numpy`, `matplotlib` y `seaborn` pueden ser un buen inicio.
- Realice una exploración inicial de los datos:
  - `head`
  - `describe`
  - `info`
  - `tail`
- Realice una exploración univariada de los datos e identifique si hay variables que tengan correlaciones altas utilizando una matriz de correlación.
- Concluya.

## Enriquecimiento de los datos

- Observe las variables y determine si puede sintetizar algunas de ellas en menos variables (descuentos, por ejemplo).

## Análisis de componentes principales

- Lleve a cabo un PCA conservando un mínimo del 80% de la varianza de los datos.

## Clusterización

- Lleve a cabo un proceso de clusterización haciendo uso de `K-Means`. Tenga en cuenta el `davies_bouldin_score` para seleccionar el número adecuado de clústers.

## Análisis de clústers

- Dentro del dataframe original, cree una columna que contenga los clústers encontrados en el punto anterior.
- Realice un análisis gráfico bivariado entre la columna con los clústers encontrados y las demás variables.
- Concluya.
