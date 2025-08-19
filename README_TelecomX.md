# Desafío: Análisis de Evasión de Clientes en Telecom X

## 📄 Descripción del Proyecto

Este proyecto consiste en un análisis exploratorio de datos (EDA) sobre la evasión de clientes (*churn*) en la empresa de telecomunicaciones ficticia "Telecom X". El objetivo principal es identificar los factores y patrones clave que caracterizan a los clientes que abandonan el servicio.

El análisis abarca desde la extracción y limpieza de los datos hasta la visualización de insights y la generación de un informe con conclusiones. El resultado final es un conjunto de datos limpio y una serie de hallazgos que servirán como base para que el equipo de Ciencia de Datos pueda construir un modelo predictivo de churn.

## 📁 Estructura del Repositorio

* `TelecomX_LATAM.ipynb`: Notebook de Jupyter con todo el proceso de análisis, desde la carga de datos hasta las conclusiones y visualizaciones.
* `TelecomX_Data.json`: El archivo de datos brutos en formato JSON, consumido originalmente desde una API.
* `TelecomX_diccionario.md`: Diccionario de datos que describe cada una de las columnas del dataset.
* `README.md`: Este archivo, que documenta el proyecto.

## 🛠️ Metodología

El análisis se desarrolló siguiendo los siguientes pasos estructurados:

1.  **Extracción de Datos**: Se obtuvieron los datos en formato JSON desde la API proporcionada.
2.  **Carga y Normalización**: Los datos JSON se cargaron y normalizaron en un DataFrame de Pandas para facilitar su manipulación.
3.  **Limpieza y Preprocesamiento**:
    * Se renombraron las columnas a un formato más legible y consistente.
    * Se estandarizaron los valores categóricos (ej. `Yes`/`No` a `Sí`/`No`).
    * Se manejaron los valores nulos, eliminando las filas correspondientes para garantizar la integridad del análisis.
4.  **Análisis Exploratorio de Datos (EDA)**:
    * Se analizó la distribución general de la evasión de clientes.
    * Se crearon visualizaciones para comparar la tasa de evasión entre diferentes segmentos de clientes, basadas en variables categóricas.

## 📈 Principales Hallazgos

El análisis reveló patrones claros que identifican a los clientes con mayor riesgo de evasión:

* **El Tipo de Contrato es el factor más decisivo**: Los clientes con contratos **mes a mes** presentan una tasa de evasión drásticamente superior a la de los clientes con contratos de 1 o 2 años.
* **La Antigüedad y los Cargos Mensuales son clave**: Los clientes **más nuevos** y aquellos con **cargos mensuales más elevados** son significativamente más propensos a cancelar el servicio.
* **El Servicio de Fibra Óptica presenta una mayor tasa de Evasión**: Contraintuitivamente, los clientes con el servicio de fibra óptica, que es premium, tienden a evadir más. Esto podría sugerir problemas de expectativas, estabilidad del servicio o una relación costo-beneficio percibida como desfavorable.

## 🚀 Tecnologías Utilizadas

* **Lenguaje**: Python 3
* **Bibliotecas Principales**:
    * **Pandas**: Para la manipulación y análisis de datos.
    * **Requests**: Para la extracción de datos desde la API.
    * **Matplotlib** y **Seaborn**: Para la creación de visualizaciones estáticas e informativas.
* **Entorno de Desarrollo**: Google Colab (Jupyter Notebook).

## 💻 Cómo Ejecutar el Proyecto

1.  **Clonar el repositorio** (si aplica) o descargar los archivos.
2.  **Abrir el notebook `TelecomX_LATAM.ipynb`** en un entorno compatible como Google Colab o Jupyter local.
3.  **Instalar las dependencias** (si se ejecuta localmente):
    ```bash
    pip install pandas requests matplotlib seaborn jupyterlab
    ```
4.  **Ejecutar las celdas** del notebook en orden secuencial.

> **Nota**: La celda de extracción de datos requiere la URL de la API. Si la API no está disponible, el análisis se puede replicar cargando los datos desde el archivo `TelecomX_Data.json` incluido en este repositorio.
