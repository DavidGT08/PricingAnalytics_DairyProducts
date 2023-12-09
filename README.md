# Data Analytics y Business Analytics de productos lácteos

## Resumen

Las tarjetas de calificación crediticia son un método de control de riesgos habitual en el sector financiero. En general, las tarjetas de puntuación de crédito se basan en datos históricos. En la actualidad, con el desarrollo de los algoritmos de aprendizaje automático. Se han introducido en la puntuación de tarjetas de crédito métodos más predictivos como Boosting, Random Forest y Support Vector Machines. Sin embargo, estos métodos no suelen ser muy transparentes. Puede ser difícil proporcionar a los clientes y a los reguladores una razón para el rechazo o la aceptación. Los datos se toman del [dataset en Kaggle](https://www.kaggle.com/datasets/rikdifos/credit-card-approval-prediction).


## Definición del Problema

Predecir la aprobación de una tarjeta de crédito de un cliente de acuerdo con su registro de solicitud.

### Flujo del Proceso
El proceso del proyecto, a grandes rasgos se presenta a continuación, se desarrollaron documentos en formato markdown para seguir este proceso:

1. [Exploración y Limpieza de datos](./src/1_Exploracion_Limpieza.ipynb)
2. [Analisis cualitativo del application record](./src/2_Analisis_application_record.ipynb). 
3. [Analisis cuantitativo del credit record](src/3_Analisis_credit_record.ipynb)
4. [Etiquetado de datos](./src/4_Etiquetado.ipynb). Con base en el análisis cuantitativo y cualitativo de los dos datasets, se da una etiqueta a los datos.
5. [Analisis Estadistico de clientes](./src/5_Analisis_Estadistico_Clientes.ipynb)
6. [Clasificadores mediante Machine Learning](./src/6_Machine_Learning_Clasificadores.ipynb) Usamos Naïve Bayes, Árboles de Decisión para comparar los resultados de clasificación.
7. [Prueba con SVM](./src/7_Machine_Learning_Prueba_SVM_RBF.ipynb) Utilizamos un tercer clasificador para observar sus resultados.

## Descripción Técnica

1. Comenzamos explorando el dataset para revisar los tipos de datos qué tenemos y qué limpieza es necesaria.
2. De los datos personales que los clientes del banco compartieron para la aprobación del crédito, hacemos gráficas para hacer un perfil promedio de los aplicantes.
3. Ahora, realizamos el análisis del compartamiento crediticio pasado de los aplicantes.
4. Con estos dos análisis anteriores, podemos dar un etiquetado preliminar de los datos.
5. Hacemos un análisis estadísticos de los aplicantes para crear un perfil promedio de la gente que está pidiendo el crédito.
6. De los modelos supervisados, vamos a utilizar Naïve Bayes, Árboles de Decisión y SVM para revisar cuál da mejores resultados en la clasificación



## Integrantes

El proyecto fue realizado en equipo conformado de la siguiente manera:

* Luis Gerardo Soria Silva
* Abel Rodruiguez Santillan
* David Gómez Torres
