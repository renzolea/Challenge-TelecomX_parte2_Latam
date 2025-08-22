# ⭐️ Proyecto: Análisis de Cancelación de Clientes en Telecom X  

⭐️ **Descripción General**  
Este proyecto analiza la cancelación de clientes en Telecom X, con el objetivo de predecir qué usuarios tienen mayor probabilidad de abandonar el servicio. A través de la limpieza de datos, análisis exploratorio y modelado predictivo, se buscan insights estratégicos para mejorar la retención de clientes.  

⭐️ **Archivos del Proyecto**  
- `TelecomX_LATAM_2.ipynb` → Notebook que contiene el análisis completo.  
- `data.csv` → Datos preprocesados.  
- `README.md` → Documentación explicativa.  

⭐️ **Herramientas y Librerías**  
- Python 3.x  
- Pandas, NumPy  
- Matplotlib, Seaborn, Plotly  
- Scikit-learn  
- Jupyter Notebook  

⭐️ **Configuración del Entorno**  
⭐️ Flujo Metodológico

- Preparación y limpieza de datos.  
- Análisis exploratorio con visualizaciones.  
- División del conjunto de datos en entrenamiento (70%) y prueba (30%).  
- Construcción de modelos predictivos: Árbol de Decisión y Random Forest.  
- Evaluación de los modelos utilizando Exactitud (Accuracy), Precisión, Recall, F1-score y matriz de confusión.  
- Identificación de las variables más influyentes para la predicción de cancelaciones.  

⭐️ Resultados Comparativos

| Modelo           | Exactitud | Precisión | Recall  | F1-score |
|-----------------|-----------|-----------|---------|----------|
| Árbol de Decisión | 72.41%    | 48.06%    | 48.66%  | 0.4836   |
| Random Forest     | 78.32%    | 61.17%    | 50.27%  | 0.5519   |

⭐️ Interpretación de Resultados

- Random Forest supera al Árbol de Decisión en Exactitud, Precisión y F1-score, mostrando menor error al predecir cancelaciones.  
- El Recall en ambos modelos es cercano al 50%, lo que indica que aún hay espacio para mejorar la detección de clientes que realmente cancelan.  

⭐️ Overfitting / Underfitting

- **Árbol de Decisión**: Rendimiento limitado (72% de Exactitud), probablemente presenta underfitting por ser un modelo demasiado simple.  
  - 🔧 Recomendación: ajustar `max_depth` entre 5 y 10, incrementar `min_samples_split` y `min_samples_leaf`.  
- **Random Forest**: Buena generalización (78% de Exactitud), aunque el bajo Recall refleja tendencia hacia la clase mayoritaria (clientes que no cancelan).  
  - 🔧 Recomendación: usar `class_weight="balanced"`, aumentar `n_estimators` (≥300), ajustar `max_depth` y `max_features`, y optimizar con GridSearchCV.  

⭐️ Variables Más Influyentes

- Antigüedad del cliente (Tenure)  
- Tipo de contrato  
- Cargos mensuales  
- Método de pago  
- Tipo de servicio de internet  

⭐️ Conclusiones y recomendaciones

- Random Forest se confirma como el modelo más confiable para predecir cancelaciones, equilibrando Exactitud y Precisión sin perder capacidad de detección.  
- Clientes de mayor riesgo: aquellos con contratos mensuales, baja antigüedad y cargos mensuales altos.  
- Estrategias de retención recomendadas: planes de fidelización temprana, incentivos para contratos largos, ajustes en la estructura de precios y personalización de la experiencia según el tipo de servicio.  

⭐️ Autor

Proyecto desarrollado por **Renzo Lea** en el marco del reto de Ciencia de Datos de Alura Latam.  

© 2025 – Análisis de Cancelación de Clientes – Proyecto de Ciencia de Datos
