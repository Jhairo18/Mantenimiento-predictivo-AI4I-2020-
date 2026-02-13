# Mantenimiento Predictivo Industrial (AI4I 2020) ⚙️

Este proyecto implementa un sistema de clasificación para la detección temprana de fallas en maquinaria industrial utilizando el dataset **AI4I 2020 Predictive Maintenance**. El objetivo principal es comparar diversos modelos de Machine Learning para identificar fallas antes de que ocurran, optimizando el balance entre precisión y detección de eventos críticos.

## 🚀 Resumen del Proyecto

El mantenimiento predictivo es un reto de clasificación desbalanceada. En este repositorio se realiza un flujo completo de Ciencia de Datos: desde el análisis exploratorio (EDA) hasta el despliegue de un modelo robusto basado en **Random Forest**.

### Tecnologías Utilizadas
* **Lenguaje:** Python 3.x
* **Librerías:** Pandas, NumPy, Scikit-Learn, TensorFlow (DNN), Matplotlib, Seaborn.
* **Métricas:** Confusion Matrix, ROC-AUC, Recall, Precision.

## 📊 Metodología y Desarrollo

### 1. Análisis Exploratorio (EDA)
Se analizaron variables termodinámicas (temperatura del aire, del proceso, torque y velocidad de rotación). Se identificó un fuerte desbalance de clases, donde las fallas representan una pequeña fracción del total de datos, lo cual guio la estrategia de evaluación.

### 2. Modelado y Comparación
Se evaluaron y compararon las siguientes arquitecturas:
* **Regresión Logística:** (Línea base).
* **Árboles de Decisión:** Recall más considerable, pero con tendencia al sobreajuste (overfitting).
* **Redes Neuronales Densas (DNN):** Evaluadas para capturar relaciones no lineales.
* **Random Forest (Modelo Final):** Seleccionado como el mejor balanceador.

### 3. Selección del Modelo (Criterio Técnico)
A pesar de que el Árbol de Decisión mostró un Recall superior en algunas pruebas, se optó por **Random Forest** debido a:
* **Mayor estabilidad en el AUC (Area Under the Curve):** Garantiza una mejor separación de clases en datos no vistos.
* **Reducción de Varianza:** Menor riesgo de falsos positivos costosos para la operación industrial.
* **Robustez ante el desbalance:** Mejor manejo de la importancia de características (Feature Importance).

> **Nota técnica:** El modelo final alcanzó un Recall de **0.63**. Aunque es un punto de mejora, se priorizó la consistencia del AUC para asegurar que el modelo sea confiable en un entorno de producción real.

## 🛠️ Cómo utilizar este repositorio
1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/Jhairo18/Mantenimiento-predictivo-AI4I-2020-.git](https://github.com/Jhairo18/Mantenimiento-predictivo-AI4I-2020-.git)
