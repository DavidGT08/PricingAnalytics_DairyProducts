# Data Analytics y Business Analytics de productos lácteos

## Resumen

Mediante la aplicación de conceptos del Data Analytics hacer un modelo para de inteligencia artificial
para hacer la predicción de venta de Suero y Lactosa con el fin de determinar el mejor precio a partir de
precios dinámicos. Los datos del precio de Suero y Lactosa se obtienen al hacer Web scrpping, el método se describe en los archivos.


## Definición del Problema

Obtener datos sobre la venta de Suero y Lactosa para responder preguntas relacionadas al precio dinámico de los lácteos con respecto a su disponibilidad de inventario. Además, hacer un forecasting de 4 semanas usando el histórico de precios.


## Descripción Técnica

1. **Obtención de los datos:**
    Realizamos un webscrapping de las bases de datos que hay sobre precios de lácteos, formateamos los datos para poder trabajarlos y eliminamos registros inecesarios. Guardamos el resultado en un dataframe y posteriormente en un archivo .csv. [Web scrapping](./data/data_pricing.csv)
2. **Visualizaciones:**
   Para tener un entendimiento global del comportamiento de los datos, realizamos gráficas que nos dejen ver el comportamiento temportal de los precios.
3. **Implementación de LSTM:**
  Creamos con un modelo para hacer forescating de los precios de suero y lactosa, usando una red LSTM con 500 épocas :

    3.1. [Suero](./models/model_whey.pt)
  
    3.2. [Lactosa](./models/model_lactose.pt)
   
4. **Predicciones:**
   Según la bibliográfia, para una predicción de cierto intervalo de tiempo, debemos ocultar de la serie de tiempo el mismo intervalo. Por ello, quitamos 4 semanas de los registros que tenemos en la serie temporal.

   4.1. Hacemos un análisis de residuos para observar si existe un patrón que nos indique un error sistemático.
   
5. **Precio dinámico:**
   
   5.1. *Datos sinteticos.* Los datos tienen 2mil toneladas como mínimo y 10mil como máximo, por         producto. La media es de 5mil, aproximadamente; desviación estándar de ±2mil toneladas           para lactosa y ±1.5 mil toneladas para suero (whey).

   5.2. *Compra condicionada.* La compra de un solo cliente está limitada a menos del 50% del             inventario total. Hay dos tipos de clientes, un cliente A y uno B. El cliente B
        está limitado a un número limitado de toneladas en espera del cliente premium.
 
7. **Drifts:**
   Evidently es una biblioteca Python de código abierto para científicos de datos e ingenieros de ML. Ayuda a evaluar, probar y supervisar datos y modelos de ML desde la validación hasta la producción. Funciona con datos tabulares, de texto e incrustaciones.
   


## Integrantes

El proyecto fue realizado en equipo conformado de la siguiente manera:

* Luis Gerardo Soria Silva
* Abel Rodruiguez Santillan
* David Gómez Torres
