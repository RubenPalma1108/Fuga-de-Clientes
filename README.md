# Modelo de Machine Learning para la Predicción de Fuga de Clientes (Customer Churn)

## 📝 Descripción del Proyecto

Este proyecto se enfoca en desarrollar un modelo de clasificación para predecir qué clientes de una empresa de telecomunicaciones son más propensos a cancelar su contrato (churn). Identificar a estos clientes de manera proactiva permite a la empresa diseñar estrategias de retención efectivas y reducir la pérdida de ingresos.

El objetivo principal es construir y evaluar diferentes modelos de Machine Learning para encontrar el que mejor prediga la fuga de clientes, así como interpretar los resultados para entender los factores clave detrás de este comportamiento.

## 🛠️ Herramientas Utilizadas

* **Lenguaje de Programación:** Python 3.x
* **Librerías Principales:**
    * **Pandas:** Para la carga y manipulación de datos.
    * **Scikit-learn:** Para el preprocesamiento de datos, entrenamiento y evaluación de modelos (Regresión Logística, Random Forest, etc.).
    * **Matplotlib & Seaborn:** Para la visualización de datos y resultados del modelo (matriz de confusión, curva ROC).
* **Entorno de Desarrollo:** Jupyter Notebook / Google Colab

## 📂 Estructura del Repositorio

```
.
├── 📁 data/
│   └── telco_customer_churn.csv    # Dataset de IBM
├── 📁 notebooks/
│   └── churn_prediction_model.ipynb # Notebook con el desarrollo del modelo
└── README.md                       # Este archivo
```

## 🔬 Metodología

1.  **Análisis Exploratorio de Datos (EDA):** Se analizó la distribución de las variables y se compararon las características de los clientes que se quedaron (`Churn=No`) frente a los que se fueron (`Churn=Yes`).
2.  **Preprocesamiento de Datos (Data Preprocessing):**
    * Codificación de variables categóricas utilizando One-Hot Encoding.
    * Escalado de variables numéricas con `StandardScaler` para normalizar su rango.
3.  **Construcción del Modelo:**
    * División del dataset en conjuntos de entrenamiento (80%) y prueba (20%).
    * Entrenamiento de tres modelos de clasificación:
        1.  **Regresión Logística:** Como modelo base.
        2.  **Árbol de Decisión:** Para una fácil interpretación.
        3.  **Random Forest:** Para mejorar la precisión y robustez.
4.  **Evaluación del Modelo:** Se evaluó el rendimiento de cada modelo utilizando las siguientes métricas:
    * **Matriz de Confusión:** Para entender los tipos de errores (Falsos Positivos y Falsos Negativos).
    * **Accuracy, Precision, Recall y F1-Score.**
    * **Curva ROC y el área bajo la curva (AUC):** Para medir la capacidad de discriminación del modelo.

## 📊 Resultados

El modelo de **Random Forest** obtuvo el mejor rendimiento general con un **AUC de 0.84** en el conjunto de prueba. Los factores más influyentes para predecir la fuga de clientes fueron:

1.  **Tipo de Contrato:** Los clientes con contratos mes a mes son mucho más propensos a irse.
2.  **Antigüedad (Tenure):** Los clientes nuevos tienen una mayor probabilidad de fuga.
3.  **Servicios de Soporte Técnico:** La ausencia de servicios como soporte técnico o seguridad online está correlacionada con una mayor tasa de churn.

## 🚀 Cómo Ejecutar este Proyecto

1.  Clona este repositorio:
    ```bash
    git clone [https://github.com/tu-usuario/nombre-del-repositorio.git](https://github.com/tu-usuario/nombre-del-repositorio.git)
    ```
2.  Navega al directorio del proyecto:
    ```bash
    cd nombre-del-repositorio
    ```
3.  Instala las dependencias:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn
    ```
4.  Abre el notebook `churn_prediction_model.ipynb` para ejecutar el código paso a paso.

## ✒️ Autor

* **[Tu Nombre]** - [Tu Perfil de LinkedIn o GitHub]
