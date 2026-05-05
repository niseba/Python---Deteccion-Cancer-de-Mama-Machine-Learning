# 🎗️ Detección de Cáncer de Mama con Machine Learning — SVM

## 📌 Descripción General

Proyecto de clasificación supervisada para la detección de tumores malignos vs. benignos a partir del **Wisconsin Breast Cancer Dataset**. El enfoque central del proyecto está en la **selección rigurosa de características mediante criterios estadísticos** y la **optimización sistemática del modelo**, logrando una precisión del **98.68%**.

---

## 📁 Dataset

- **Fuente:** Wisconsin Breast Cancer Dataset
- **Variable objetivo:** Diagnóstico (Maligno / Benigno)
- **Variables predictoras:** Características morfológicas del núcleo celular (radio, textura, perímetro, área, suavidad, entre otras)

---

## ⚙️ Tecnologías

Python · Pandas · NumPy · Scikit-learn · Matplotlib · Seaborn · Jupyter Notebook

---

## 🔍 Análisis Exploratorio y Selección de Características (EDA)

La selección de características fue el núcleo metodológico del proyecto, aplicando múltiples criterios estadísticos para evaluar la utilidad de cada variable:

- **Correlaciones entre variables:** identificación y eliminación de características redundantes con alta colinealidad
- **Pairplots:** visualización de relaciones entre pares de variables para detectar separabilidad entre clases
- **Solapamiento de distribuciones:** evaluación del grado en que las distribuciones de cada clase se superponen por variable
- **Correlación con la variable objetivo:** cuantificación del poder predictivo individual de cada característica
- **No separabilidad:** descarte de variables que no aportan poder discriminativo entre clases

Este proceso garantizó que el modelo recibiera únicamente las características con mayor valor predictivo, reduciendo ruido y mejorando la generalización.

---

## 🧪 Preprocesamiento y Modelado

### Normalización
- Escalado estandarizado (StandardScaler) para garantizar equidad en la métrica de distancia del SVM
- Validación cruzada para determinar el número óptimo de folds y el test size que maximiza la generalización del modelo

### Modelo implementado
**Support Vector Machine (SVM)** — clasificador de alto desempeño en espacios de alta dimensionalidad, especialmente efectivo en problemas de clasificación binaria con datos médicos.

### Optimización de hiperparámetros
Se implementó **GridSearchCV** para búsqueda exhaustiva de los hiperparámetros óptimos del SVM, maximizando el desempeño mediante validación cruzada.

---

## 📊 Resultados

| Métrica | Valor |
|---|---|
| Precisión (Accuracy) | **98.68%** |
| F1-score | ~1.0 |
| Recall | ~1.0 |

La matriz de confusión mostró un resultado bien balanceado, con mínimos falsos negativos — críticos en contextos de diagnóstico médico donde no detectar un caso positivo tiene consecuencias graves.

---

## 📌 Conclusión

El modelo SVM optimizado con GridSearchCV alcanzó un 98.68% de precisión, respaldado por una selección de características estadísticamente fundamentada y una evaluación robusta. Este proyecto demuestra que la calidad del análisis previo al modelado — no solo el algoritmo — es determinante en el desempeño final.

---

## 🚀 Habilidades Demostradas

✔️ Selección de características con criterios estadísticos múltiples (correlación, solapamiento, separabilidad)
✔️ Análisis exploratorio estadístico (EDA) con pairplots y distribuciones por clase
✔️ Normalización y escalado estandarizado
✔️ Implementación de Support Vector Machine (SVM)
✔️ Optimización de hiperparámetros con GridSearchCV
✔️ Validación cruzada para generalización del modelo
✔️ Evaluación con accuracy, F1-score, recall y matriz de confusión
✔️ Documentación reproducible en Jupyter Notebook

---

> 🎯 **Nota:** Desarrollado como primer proyecto en Python, este trabajo refleja desde el inicio un enfoque estadístico riguroso — priorizando la comprensión del dato sobre la ejecución mecánica del modelo.
