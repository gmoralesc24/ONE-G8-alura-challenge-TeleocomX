# Desafío Telecom X: Análisis de Evasión de Clientes en Python

¡Bienvenido al repositorio del Desafío Telecom X! Este proyecto forma parte del curso de Data Science de Alura Latam, enfocado en la aplicación práctica de habilidades de ETL (Extract, Transform, Load) y análisis exploratorio de datos (EDA) para entender y abordar la alta tasa de evasión de clientes en una empresa de telecomunicaciones.

## 🎯 Propósito del Análisis

El objetivo principal de este proyecto es realizar un análisis exhaustivo de los datos de clientes de Telecom X para identificar los factores y patrones que contribuyen a la "cancelación" (churn) del servicio. El propósito final es entregar un conjunto de datos limpio y un informe de hallazgos iniciales al equipo de ciencia de datos, quienes lo utilizarán para construir un modelo predictivo de churn.

Este análisis busca responder preguntas clave como:

* ¿Quiénes son los clientes que cancelan?

* ¿Qué características o comportamientos están asociados con la evasión?

* ¿Cómo se pueden utilizar estos insights para desarrollar estrategias de retención?

## 📁 Estructura del Proyecto y Organización de Archivos

Este repositorio contiene:

* `TelecomX_LATAM.ipynb`: El cuaderno Jupyter/Colab principal donde se realiza todo el proceso de ETL y el análisis exploratorio de datos.

* **Datos Originales:** Los datos utilizados en este análisis se extraen directamente de una API en formato JSON, no se almacenan localmente en este repositorio como archivos separados.

La estructura del código dentro del `TelecomX_LATAM.ipynb` está organizada en las siguientes secciones principales, siguiendo el flujo ETL:

1.  **📌 Extracción:** Se realiza la conexión y descarga de los datos desde la API pública de Telecom X.

2.  **🔧 Transformación:** Incluye la limpieza de nombres de columnas, el manejo de valores nulos (relleno por la mediana), la conversión de tipos de datos (numéricos, binarios, categóricos), y la eliminación de registros duplicados para asegurar la consistencia y calidad de los datos.

3.  **📊 Carga y Análisis:** Se lleva a cabo el análisis exploratorio de datos (EDA) utilizando estadísticas descriptivas y visualizaciones (histogramas, boxplots, gráficos de barras y mapas de calor de correlación) para entender la distribución de las variables y su relación con la cancelación.

4.  **📄 Informe Final:** Un resumen conciso de las conclusiones clave del análisis y las posibles razones detrás de la evasión de clientes, dirigido al equipo de ciencia de datos.

## 📈 Ejemplos de Insights Obtenidos

El análisis exploratorio de datos reveló varios factores críticos asociados con la evasión de clientes en Telecom X:

* **Antigüedad del Cliente (`antiguedad`):** Los clientes con menor antigüedad (nuevos clientes) muestran una tasa de cancelación significativamente más alta.

    * *Insight Clave:* Los primeros meses de servicio son cruciales para la retención.

* **Tipo de Contrato (`contrato`):** Los clientes con contratos mensuales (`Month-to-month`) tienen una propensión mucho mayor a cancelar en comparación con aquellos con contratos a largo plazo (uno o dos años).

    * *Insight Clave:* La flexibilidad del contrato influye directamente en la lealtad del cliente.

* **Servicios Adicionales:** La ausencia de servicios como seguridad online, copia de seguridad, protección de dispositivo y soporte técnico está fuertemente correlacionada con una mayor tasa de cancelación. Los problemas percibidos con el servicio de internet de fibra óptica también contribuyen al churn.

    * *Insight Clave:* Los servicios de valor añadido y la calidad de los servicios principales son fundamentales para la satisfacción.

* **Método de Pago (`metodo_pago`):** Los clientes que utilizan el `Electronic check` (`cheque_electronico`) como método de pago tienen una tasa de cancelación notablemente más alta.

    * *Insight Clave:* Posibles fricciones o características subyacentes de los usuarios de este método de pago.

* **Precio Mensual (`precio_mensual`):** Los clientes que cancelan a menudo tienen precios mensuales más altos.

    * *Insight Clave:* Percepción de valor o competitividad del precio.

Para una comprensión visual de estos hallazgos, se recomienda añadir capturas de pantalla de los gráficos más relevantes obtenidos del notebook. Puedes insertar imágenes directamente usando la sintaxis `![Descripción de la imagen](ruta/a/tu/imagen.png)`, o alojarlas en el repositorio o un servicio de hosting de imágenes. Ejemplos de gráficos clave incluyen: Distribución de Churn, Histograma/Boxplot de Antigüedad vs. Churn, Gráfico de barras de Contrato vs. Churn, entre otros.

## 🚀 Instrucciones para Ejecutar el Notebook

Para replicar y explorar este análisis en tu propio entorno:

1.  **Accede a Google Colab:**

    * Abre tu navegador y ve a [Google Colab](https://colab.research.google.com/).

2.  **Abrir el Cuaderno:**

    * Haz clic en `Archivo` (File) -> `Abrir cuaderno` (Open notebook).

    * En la ventana emergente, selecciona la pestaña `GitHub`.

    * Pega la URL de este repositorio. **Importante:** Asegúrate de reemplazar `https://github.com/tu-usuario/telecom-x-challenge` con la URL real de **tu propio repositorio** en GitHub para acceder al cuaderno.

    * Selecciona el archivo `TelecomX_LATAM.ipynb` y haz clic en `Abrir`.

3.  **Ejecutar las Celdas:**

    * Una vez que el cuaderno esté abierto en Colab, puedes ejecutar cada celda de forma secuencial haciendo clic en el botón de "Play" al lado de cada celda, o puedes ejecutar todas las celdas yendo a `Entorno de ejecución` (Runtime) -> `Ejecutar todas` (Run all).

**¡Esperamos que este análisis sea un buen punto de partida para resolver el problema de evasión de clientes en Telecom X!**
