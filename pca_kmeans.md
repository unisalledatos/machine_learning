# Ejercicio

`ID`: identificador único del cliente
`Year_Birth`: año de nacimiento del cliente
`Education`: nivel educativo del cliente
`Marital_Status`: estado civil del cliente
`Income`: ingreso anual del hogar del cliente
`Kidhome`: número de niños en el hogar del cliente
`Teenhome`: número de adolescentes en el hogar del cliente
`Dt_Customer`: fecha de inscripción del cliente en la empresa
`Recency`: número de días desde la última compra del cliente
`Complain`: 1 si el cliente se quejó en los últimos 2 años, 0 en caso contrario

`MntWines`: cantidad gastada en vino en los últimos 2 años
`MntFruits`: cantidad gastada en frutas en los últimos 2 años
`MntMeatProducts`: cantidad gastada en carne en los últimos 2 años
`MntFishProducts`: cantidad gastada en pescado en los últimos 2 años
`MntSweetProducts`: cantidad gastada en dulces en los últimos 2 años
`MntGoldProds`: cantidad gastada en oro en los últimos 2 años

`NumDealsPurchases`: número de compras realizadas con descuento
`AcceptedCmp1`: 1 si el cliente aceptó la oferta en la primera campaña, 0 en caso contrario
`AcceptedCmp2`: 1 si el cliente aceptó la oferta en la segunda campaña, 0 en caso contrario
`AcceptedCmp3`: 1 si el cliente aceptó la oferta en la tercera campaña, 0 en caso contrario
`AcceptedCmp4`: 1 si el cliente aceptó la oferta en la cuarta campaña, 0 en caso contrario
`AcceptedCmp5`: 1 si el cliente aceptó la oferta en la quinta campaña, 0 en caso contrario
`Respuesta`: 1 si el cliente aceptó la oferta en la última campaña, 0 en caso contrario


`NumWebPurchases`: número de compras realizadas a través del sitio web de la empresa
`NumCatalogPurchases`: número de compras realizadas utilizando un catálogo
`NumStorePurchases`: número de compras realizadas directamente en tiendas
`NumWebVisitsMonth`: número de visitas al sitio web de la empresa en el último mes

## Importación, carga y exploración inicial

- Descargue los siguientes [datos](https://raw.githubusercontent.com/unisalledatos/machine_learning/main/marketing_campaign.csv) y léalos en Google Colab.
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
