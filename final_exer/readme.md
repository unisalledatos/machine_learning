# Ejercicio final

El siguiente [dataset]() contiene información del consumo de un plan de telefonía móvil de 3214 usuarios en un mes determinado. 

- `llamadas`: número de llamadas realizadas
- `minutos`: número de minutos consumidos
- `mensajes`: número de mensajes enviados
- `datos_usados`: volumen datos utilizados en megabytes
- `plan`: nombre del plan al que pertenece cada usuario

El objetivo del proyecto es crear un modelo que, a partir de las características observadas, permita realizar una recomendación del plan más adecuado. Para ello, se sugiere llevar a cabo los siguientes pasos después de importar tanto las librerías como el dataset:

1. Análisis exploratorio de datos.
2. Preprocesamiento.
3. Codificación (transformación en variable dummy) de la variable objetivo (variable `plan`).
4. Separación en variables independientes y variable de respuesta.
5. Separación en conjuntos de entrenamiento y testeo (20% de testeo con random_state=12345).
6. Modelamiento y optimización de hiperparámetros (puede probar tantos como considere necesarios)
7. Prueba del modelo. Tome el mejor modelo y realice una predicción sobre el conjunto de testeo. Calcule el `f1_score`.
8. Selección del modelo.
9. Conclusiones.

El proyecto será evaluado única y exclusivamente a partir de la métrica `f1_score` siguiendo se muestra en la siguiente tabla (lo primero que se cumpla):

|f1 score | Nota|
|---|---|
|<0.6|2.5|
|<0.7|3|
|<0.75|3.5|
|<0.8|4.0|
|<0.85|4.5|
|>=0.85|5|

Evite el plagio. Puede utilizar CUALQUIER herramienta existente para alcanzar el objetivo.
