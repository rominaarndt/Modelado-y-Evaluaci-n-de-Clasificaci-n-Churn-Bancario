# Modelado-y-Evaluaci-n-de-Clasificaci-n-Churn-Bancario
# Predicción de Abandono de Clientes (Churn Bancario) — Modelado y Evaluación

## Descripción del Problema
Este proyecto aborda un problema de **clasificación binaria** orientado a predecir si un cliente bancario abandonará el servicio (`Exited = 1`) o permanecerá (`Exited = 0`) utilizando el dataset clásico **Bank Customer Churn Modeling** (`Churn_Modelling.csv`, 10.000 registros).

Desde la perspectiva del negocio, identificar de forma anticipada a los clientes con riesgo de fuga es clave para activar acciones de retención. En este contexto, el **Recall** sobre la clase positiva (`Exited = 1`) cobra especial relevancia: un **falso negativo** (predecir que el cliente se queda cuando en realidad se va) implica perder ingresos recurrentes y asumir un costo de readquisición mayor, mientras que un **falso positivo** (activar una campaña de retención sobre un cliente que no iba a irse) tiene un costo operativo o promocional considerablemente menor.

## Estructura del Repositorio
* `modelado_metricas.ipynb`: Notebook de Jupyter con la carga de datos, división entrenamiento/prueba (`80/20` estratificada), pipeline de preprocesamiento (`ColumnTransformer` con imputación y escalado/codificación sin fuga de datos), entrenamiento de **Logistic Regression** y **Random Forest**, cálculo de métricas y visualización de matrices de confusión.
* `.gitignore`: Reglas para excluir entornos virtuales (`.venv/`), caché de Python (`__pycache__/`) y checkpoints de Jupyter (`.ipynb_checkpoints/`).
* `README.md`: Documentación del proyecto, instrucciones de ejecución y resumen de resultados.

## Instrucciones de Ejecución
1. **Clonar el repositorio y ubicarse en la carpeta del proyecto:**
   ```bash

    Crear y activar un entorno virtual en Python:
   python -m venv .venv
# En Windows (PowerShell):
.\.venv\Scripts\Activate.ps1
   git clone <URLhttps://github.com/rominaarndt/Modelado-y-Evaluaci-n-de-Clasificaci-n-Churn-Bancario-DEL-REPOSITORIO>
   cd <modelado_metricas.ipynb>

   Instalar las dependencias necesarias:
   
   pip install pandas numpy scikit-learn matplotlib jupyter

   Abrir y ejecutar el notebook:

Abrí modelado_metricas.ipynb en Visual Studio Code o Jupyter Notebook.

Ejecutá todas las celdas de principio a fin (Run All) para cargar el dataset desde la fuente remota, entrenar los modelos y generar las métricas y matrices de confusión.


   
