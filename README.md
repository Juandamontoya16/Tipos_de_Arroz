# Comparación de Modelos Supervisados usando Validación Cruzada

## Autor: Juan David Montoya Agudelo


## Descripción del Dataset

El dataset Rice Type Classification proviene de [Kaggle](https://www.kaggle.com/datasets/mssmartypants/rice-type-classification) y contiene 10,000 muestras de granos de arroz de dos variedades: Cammeo y Osmancik.  
Cada fila representa un grano, y las variables numéricas describen su forma y tamaño obtenidas mediante procesamiento de imágenes.

| Variable | Descripción |
|-----------|-------------|
| Area | Área de la superficie del grano (en píxeles²). |
| Perimeter | Perímetro del grano. |
| MajorAxisLength | Longitud del eje mayor de la elipse ajustada. |
| MinorAxisLength | Longitud del eje menor de la elipse ajustada. |
| Eccentricity | Medida de qué tan alargado es el grano. |
| ConvexArea | Área del casco convexo que cubre el grano. |
| Extent | Relación entre el área del grano y su rectángulo delimitador. |
| Class | Tipo de arroz: Cammeo u Osmancik. |

---

## Objetivo del Trabajo

El objetivo del trabajo es comparar el rendimiento de distintos modelos clásicos de clasificación supervisada utilizando validación cruzada, para identificar cuál generaliza mejor.  

Se aplicaron cinco modelos:  
- Regresión Logística  
- K-Nearest Neighbors (KNN)  
- Árbol de Decisión  
- Random Forest  
- Support Vector Machine (SVM)

El conjunto de datos se dividió en entrenamiento, validación y prueba (60/20/20), aplicando estratificación para mantener el balance entre clases.  
Se empleó estandarización (StandardScaler) como parte del pipeline de preprocesamiento.


## Principales Hallazgos y Conclusiones

- Todos los modelos obtuvieron desempeños sobresalientes con ROC AUC superiores a 0.99, lo que demuestra que las variables geométricas discriminan eficazmente entre los tipos de arroz.  
- El Random Forest fue el modelo con mejor desempeño general, alcanzando un ROC AUC = 1.0000 tanto en entrenamiento, validación, validación cruzada y prueba.   
- Esto sugiere que el modelo generaliza correctamente y que las características físicas de los granos son altamente representativas.  
- En conclusión, Random Forest es el modelo más robusto y confiable para esta tarea de clasificación.# Tipos_de_Arroz
