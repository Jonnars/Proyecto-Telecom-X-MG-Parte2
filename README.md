**Telecom X - Predicción de Churn - Parte 2**


Este proyecto forma parte de un análisis avanzado de retención de clientes para la empresa Telecom X. El enfoque principal es la aplicación de modelos de Machine Learning para predecir la evasión de clientes (churn).

🎯 **Propósito del Proyecto**
El objetivo principal es desarrollar un modelo capaz de identificar proactivamente a los clientes con alta probabilidad de cancelar su servicio. Mediante el análisis de variables demográficas, servicios contratados y datos de facturación, se busca proporcionar a la empresa herramientas para diseñar estrategias de retención efectivas.

📂 **Estructura del Proyecto**
TelecomX_LATAM_MG-PARTE2.ipynb: Cuaderno principal con el flujo completo de limpieza, modelado y evaluación.

datos_tratados.csv: Conjunto de datos procesado y listo para el modelado (cargado automáticamente desde el repositorio).

README.md: Documentación del proyecto.

🛠️ **Preparación de los Datos**
Para garantizar la calidad de las predicciones, se realizó un riguroso proceso de ingeniería de datos:

Clasificación de Variables:

Numéricas: Cargos mensuales, cargos totales y meses de permanencia.

Categóricas: Género, tipo de contrato, métodos de pago y servicios adicionales (Streaming, TechSupport, etc.).

Normalización y Codificación:

Se aplicó get_dummies para transformar variables categóricas en formatos numéricos procesables.

Se utilizó StandardScaler para normalizar las variables numéricas, asegurando que factores como los "Cargos Totales" no sesguen el modelo por su magnitud.

División de Datos: Se separaron los datos en conjuntos de Entrenamiento (80%) y Prueba (20%) utilizando train_test_split con una semilla de aleatoriedad para asegurar la reproductibilidad.

🧠 **Modelización y Decisiones**
Se evaluaron y compararon dos modelos principales:

Árbol de Decisión (Seleccionado por Desempeño): Tras ajustar la consistencia de los datos, este modelo demostró ser el más efectivo para el negocio, logrando un Accuracy del 78% y un Recall del 57%. Esto significa que es capaz de detectar a más de la mitad de los clientes en riesgo de fuga.

Regresión Logística: Aunque es estable y fácil de interpretar, presentó un Recall menor (25%), lo que la hace menos efectiva para detectar casos reales de evasión en comparación con el árbol.

📊 **Insights y Visualizaciones (EDA)**
Durante el Análisis Exploratorio de Datos, se obtuvieron hallazgos críticos:

Contratos Mensuales: Los clientes sin contrato de permanencia representan el 53% del riesgo de fuga.

Cargos Elevados: Los desertores pagan en promedio $74.44, frente a los $61.26 de los clientes leales.

Antigüedad: Se identificó una "zona crítica" de fuga antes de los 18 meses de permanencia.

🚀 **Instrucciones de Ejecución**
Para ejecutar el cuaderno en tu entorno local o en Google Colab:

Bibliotecas necesarias:
Asegúrate de tener instaladas las siguientes librerías: *pandas, scikit-learn, seaborn, matplotlib*.

🚀 **Cómo ejecutar este proyecto**

Este proyecto fue desarrollado en Google Colab. Para ejecutarlo correctamente, sigue estos pasos:

Instalar dependencias: Ejecuta la primera celda del cuaderno o asegúrate de tener instaladas las librerías en tu entorno:
 pip install pandas matplotlib seaborn scikit-learn
 
Acceso a los datos: El código ya incluye la *URL de GitHub* donde está alojado el archivo `datos_tratados.csv`. No necesitas subir ningún archivo manualmente al entorno de Colab; el cuaderno lo descargará de forma automática al iniciar.

Ejecución: Ve al menú superior de Google Colab y selecciona *Entorno de ejecución > Ejecutar todas*.

Autor: Jonatan Andrade  
