# Predicción del Consumo de los Hogares en España: Comparación entre SARIMAX y Redes Neuronales

Este repositorio contiene el código fuente y los datos utilizados en el Trabajo de Fin de Grado titulado **“Comparación entre modelos de machine learning y econométricos: Evaluación del consumo de los hogares”**.

El objetivo principal del estudio es evaluar el comportamiento predictivo de dos enfoques distintos:
- Un modelo econométrico clásico: **SARIMAX**.
- Modelos de **redes neuronales recurrentes (RNN)**, específicamente LSTM y GRU.

Ambos enfoques han sido aplicados sobre las mismas series temporales relacionadas con el consumo de los hogares en España, y comparados mediante métricas de error y análisis crítico, para determinar cuál ofrece mejores resultados en distintos contextos económicos.

---

##  Estructura del repositorio

CODIGO-TFG/
```
│
├── RNN/
│ ├── final/ # Datos finales utilizados para entrenar el modelo RNN
│ │ ├── ahorro.csv
│ │ ├── ch_anual1.csv
│ │ ├── ch_trimestral2.csv
│ │ └── tasa_ahorro.csv
│ ├── results/ # Resultados del tuning de hiperparámetros
│ │ ├── nn_hyperparam_results.csv
│ │ └── top5_hyperparams.csv
│ └── RNN.ipynb # Notebook principal con el desarrollo del modelo LSTM
│
├── SARIMAX/
│ ├── final/ # Datos preprocesados para el modelo econométrico
│ │ ├── ahorro.csv
│ │ ├── ch_trimestral2.csv
│ │ ├── df_sarimax_con_pib.csv
│ │ ├── df_sarimax_preprocesado_anual.csv
│ │ ├── df_sarimax_preprocesado_con_pib.csv
│ │ ├── df_sarimax_preprocesado.csv
│ │ ├── icc.csv
│ │ ├── PIB.csv
│ │ └── tasa_ahorro.csv
│ └── SARIMAX_TFG.ipynb # Notebook principal con el desarrollo del modelo SARIMAX
```
---

##  Modelado y notebooks

- `RNN.ipynb`: Entrenamiento de modelos de redes neuronales (LSTM y variantes). Incluye preprocesamiento, definición de arquitectura y evaluación de resultados.
- `SARIMAX_TFG.ipynb`: Implementación del modelo SARIMAX con y sin variables exógenas. Contiene análisis de estacionariedad, ACF/PACF, selección de hiperparámetros y comparación final.

⚠️ **No es necesario ejecutar los notebooks**: los resultados están completamente generados y visibles dentro de cada archivo `.ipynb`.

---

##  Datos

Todos los archivos `.csv` incluidos en las carpetas `final/` contienen:
- Series temporales trimestrales y anuales del consumo de los hogares, tasa de ahorro, PIB e ICC.
- Versiones preprocesadas para alimentar directamente los modelos SARIMAX y RNN.

---

##  Resultados de optimización (RNN)

En la carpeta `RNN/results` se encuentran:
- `nn_hyperparam_results.csv`: resultados completos del tuning de hiperparámetros.
- `top5_hyperparams.csv`: mejores combinaciones obtenidas.

---

##  Requisitos

El entorno utilizado ha sido Jupyter Notebook con bibliotecas como:
- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `statsmodels`, `pmdarima`
- `torch`

No se proporciona un entorno virtual dado que los notebooks están ejecutados y comentados paso a paso.

---

##  Licencia y uso

Este código forma parte de un proyecto académico (TFG) y se distribuye con fines educativos. Puede ser reutilizado o adaptado con fines docentes o investigativos, citando adecuadamente su procedencia.

---

##  Contacto

Autora: Teresa Álvarez de Portugal 

Universidad Alfonso X el Sabio – Grado en Ingeniería Matemática  

Trabajo de Fin de Grado – Curso 2024/2025
