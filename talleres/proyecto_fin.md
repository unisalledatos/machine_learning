# Proyecto final - 2do corte: creando una aplicación para predecir los precios de los inmuebles

Antes de empezar, asegúrese de que VSCode, git y python estén instalados en el computador.

## Inicializando el proyecto en local (0.6)

1. Cree una carpeta en donde vaya a alojar el proyecto.
2. Abra esta carpeta en VSCode.
3. Cree los siguientes documentos:
   - `requirements.txt`: en este documento va a escribir en una lista descendente el nombre de cada uno de los paquetes que utilizará en el proyecto, no incluya el paquete `pickle`.
   - `app.py`: en este archivo codificará la aplicación.
   - `model.py`: en este archivo va a entrenar el modelo.
4. Abra la terminal en VSCode (será mejor si emplea el bash de git) e inicialice el repositorio con `git init`.
5. Escriba `git add .` y después `git commit -m "first push"`.
6. Cargue el dataset `hprice.csv` encontrado en el repositorio del curso. 

## Inicializando el proyecto en la nube (0.6)

1. Cree un repositorio en GitHub, preferiblemente con el mismo nombre de la carpeta en donde está alojando el proyecto en local. El repositorio no debe contener ningún archivo.
2. Después de creado el repositorio, aparecerán algunas opciones. Tome la que coincide con su situación actual: tiene un repositorio en local y quiere llevarlo a GitHub. PISTA: son tres línea de código únicamente.
3. Vuelva a local, abra la terminal y escriba las tres línea de código.

Habrá culminado bien esta parte si puede ver los documentos de local en GitHub. De lo contrario, revise si siguió los pasos perfectamente.

## Entrenando el modelo (1.4)

1. En el archivo `model.py` cargue las librerías necesarias para entrenar modelos sobre los datos. Tenga presente que hemos visto bastantes y en este punto usted ya puede decidir cuáles probar y cómo elegir:
  - RandomForest
  - DecisionTree
  - XGBoost
  - LGBM
  Asegúrese de instalar las librerías necesarias con el comando `pip install #librería` para que no tenga problemas de ejecución.
2. Cargue los datos con ayuda de `pandas`. Instálela si aún no la ha instalado.
3. Separe los datos entre la variable dependiente `y` y las variables independientes `X`.
4. Con ayuda de `train_test_split` separe los datos en grupo de entrenamiento y grupo de testeo. El tamaño del testeo déjelo en 20%.
5. Realice optimización de hiperparámetros para cada uno de los modelos. Asegúrese de crear la grilla correcta para cada uno. La métrica a mejorar es el RMSE, asegúrese de escribirlo correctamente en el optimizador.

## Evaluación y selección del modelo (0.4)

1. Con el entrenamiento del optimizador ya realizado, evalúe los modelos en el conjunto de testeo.
2. Seleccione el modelo con la mejor métrica en testeo.
3. Guarde el modelo con ayuda del paquete `pickle`:

```python
with open("model.pickle", "wb") as f:
    pickle.dump(model, f)
```
Verifique que tiene este nuevo documento en la carpeta del proyecto.

## Creación de página web (1.0)

No es necesario el resto de los puntos para empezar a crear esta parte y, para ahorrar tiempo, se recomienda que la empiece desde el principio. La aplicación debe poseer los siguientes elementos:

1. Un título llamativo.
2. Widgets para que el usuario ingrese la información que requiere el modelo para predecir el valor del inmueble.
3. Cargue el modelo construido en la sección anterior con ayuda del paquete `pickle`:
```python
with open("model.picle", "rb") as f:
    model = pickle.load(f)
```
4. Guarde los valores obtenidos a través de los widgets en variables (nombres elocuentes facilitan el trabajo).
5. Ponga las variables en un `array` y guarde este en una nueva variable:
```python
vars = np.array([[var1, var2, var3]])
```
6. Realice la predicción e imprímala.

## Deployment (1.0)

Asegúrese de que todos los paquetes o librerías empleadas en el proyecto se encuentren en el archivo `requirements.txt`.

1. Realice un `push` a su repositorio en GitHub:
```bash
git add .
git commit -m "cualquier mensaje que quiera escribir"
git push origin main
```
2. Vaya a StreamlitShare. Abra su cuenta de GitHub y cree una nueva aplicación.
3. Seleccione el repositorio, la rama, el documento y asigne un nombre a la URL.
4. Haga clic en `Deploy`.

Todo estará en orden si su proyecto se puede ver en línea y funciona correctamente.

## Puntos extra (0.1 c/u)

1. Gráfico de exploración de la variable dependiente.
2. Gráficos de exploración de las variables independientes.
3. Heatmap para un análisis de correlación.

## Puntos extra (0.3 c/u)

1. Tabs diferentes por sección. Ejemplo: un tab para los gráficos y un tab para el modelo.
2. Columnas diferentes para los widgets.
3. Evaluación del modelo.

Toda la información necesaria se encuentra en lo realizado en clase o en internet. Puede explorar `Google`, `stackoverflow` o `ChatGPT`. Si sabe qué es lo que quiere hacer, el trabajo ya está hecho.
