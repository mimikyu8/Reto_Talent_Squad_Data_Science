# Reto Talent Squad Data Science
Mi propuesta como solución al reto de [Talent Squad](https://nuwe.io/challenge/talent-squad-data-science-i)

## Background y descripción del reto
«Aproximadamente 300 sensores están conectados al cohete y al lanzador móvil para detectar, registrar y transmitir la información». SpaceX está lanzando una nueva cadena de cohetes con un nuevo propósito de negocio, rocket-commerce. Para poder conseguirlo, Elon Musk quiere predecir el estado de los cohetes para poder ajustar costes de forma dinámica. Para ello nos ha proporcionado los datos de varios sensores y su estado. ¿El objetivo? Crea un modelo que sea capaz de predecir el estado.

El objetivo de este reto será ayudar a Elon realizando el modelado predictivo a partir de un dataset que contiene las mediciones hechas por sus sensores y tipos.

### Variables del dataset:
**Features**: El dataset contiene 6 features en 6 columnas, que son los parámetros medidos de los diferentes sensores. Estos corresponden a las vibraciones detectadas en el cohete.

**Target**: El target corresponde al 'label' que clasifica los tipos de estados del cohete en función de los features medidos por los sensores.

   * Target 0 corresponde a Estable
   * Target 1 corresponde a Turbulencia Ligera
   * Target 2 corresponde a Turbulencia Moderada
   * Target 3 corresponde a Turbulencia Severa
   * Target 4 corresponde a Turbulencia Extrema

El objetivo del reto será realizar un modelo predictivo que permita conocer el tipo de erupción que tendrá un cohete en función de las vibraciones medidas por los sensores.

Una vez se haya hecho y entrenado el modelo predictivo, este se tendrá que emplear con los features del dataset de testing 'space_X_test.csv'. Estas predicciones se tendrán que entregar en formato csv donde tendrá que aparecer tan solo una columna en la que en la primera fila sea un texto cualquiera y las predicciones empiecen en la fila 2.

La calidad de la predicción se medirá a partir del f1-score (macro).

## Archivos del repositorio
  * __main.ipynb__: Notebook que recoge todo el proceso de escoger y crear el modelo para predecir los datos.
  * __Space_X_prediction.csv__: Archivo csv que contiene las predicciones calculadas con el mejor modelo estudiado.
  * __requirements.txt__: Requerimientos de librerías, módulos y paquetes

## Modelos 
Se probaron cuatro algoritmos de clasificación, Random Forest, Logistic Regression, K Neighbors y Support Vector Machine, con un escalado previo en Robust Scaler, Quantile Transformer y Yeo-Johnson Power Transformation, así como PCA. 
