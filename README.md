# ⭐️ Telecom X – Predicción de Cancelación de Clientes (Churn)

## 💡 Introducción del Proyecto
Este proyecto aborda el desafío de **predecir la cancelación de clientes en Telecom X**, una empresa que enfrenta una tasa elevada de deserción. El objetivo principal es construir un pipeline robusto que permita anticipar qué clientes tienen mayor probabilidad de cancelar sus servicios, utilizando modelos de Machine Learning y análisis de datos para generar conclusiones estratégicas que impulsen la retención.

---

## 🎯 Objetivos del Proyecto
- Preparar y preprocesar los datos para el modelado.  
- Realizar análisis exploratorio y selección de variables clave.  
- Construir y entrenar modelos de clasificación supervisada.  
- Evaluar el rendimiento con métricas de desempeño.  
- Interpretar resultados y extraer insights estratégicos.  
- Proponer acciones de negocio para reducir la cancelación.  

---

## 🧰 Preparación de los Datos
- Archivo CSV limpio y normalizado como base.  
- Eliminación de columnas irrelevantes (ej. *customerID*, *account.Charges.Total*).  
- Codificación de variables categóricas (One-Hot Encoding y binarización).  
- Análisis de la proporción de clientes que cancelaron (churn).  
- Recomendación de aplicar técnicas de balanceo como **SMOTE** en caso de fuerte desbalance.  
- Normalización opcional para modelos sensibles a escala (Logistic Regression, KNN).  

---

## 🔎 Análisis Exploratorio y Selección de Variables
- Construcción de la **matriz de correlación** para identificar relaciones con la variable objetivo.  
- Evaluación de variables relevantes como *tiempo de contrato* y *gasto mensual* mediante gráficos (boxplots, scatter plots).  
- Selección de variables más significativas para alimentar los modelos.  

---

## 🤖 Modelado Predictivo
- División de datos en entrenamiento y prueba (70%-30%).  
- Entrenamiento de dos modelos base para comparación:  
  - **Árbol de Decisión**  
  - **Random Forest**  
- Normalización aplicada solo en modelos sensibles, no en árboles.  
- Métricas evaluadas:  
  - Exactitud (Accuracy)  
  - Precisión  
  - Recall  
  - F1-score  
  - Matriz de confusión  

---

## 📊 Resultados y Evaluación
| Modelo              | Exactitud | Precisión | Recall | F1-score |
|----------------------|-----------|-----------|--------|----------|
| Árbol de Decisión    | 72.60%    | 48.44%    | 49.91% | 49.17%   |
| Random Forest        | 78.04%    | 60.71%    | 49.02% | 54.24%   |

- **Random Forest** tuvo mejor desempeño general, especialmente en exactitud y precisión.  
- Ambos modelos muestran un **recall moderado**, lo que refleja oportunidades de mejora en la detección de clientes que realmente cancelan.  
- Posibles signos de **underfitting** en el Árbol de Decisión.  

---

## 📈 Importancia de las Variables
Las variables con mayor impacto en la predicción del churn fueron:  
- **Tenure** (tiempo como cliente).  
- **Tipo de contrato** (mensual vs anual).  
- **Cargos mensuales**.  
- **Tipo de servicio de internet**.  
- **Facturación sin papel**.  

Estas variables permiten diseñar **acciones estratégicas** para mitigar la cancelación y mejorar la fidelización.  

---

## 💡 Conclusiones y Recomendaciones Estratégicas
- Priorizar campañas de retención en **clientes nuevos** o con **contratos mes a mes**.  
- Incentivar la **contratación anual o bianual** para reforzar la fidelización.  
- Ajustar planes de precios para mejorar la **percepción de valor**.  
- Personalizar la experiencia según el **tipo de servicio contratado**.  
- Promover la **facturación digital** y comunicación proactiva para reforzar la relación con el cliente.  

---

## 📚 Recursos y Referencias
- Alura – Codificación categórica en ML.  
- Alura – Técnicas de balanceo de clases.  
- Medium – Normalización y estandarización en ML.  

---

## 👨‍💻 Autor
**Renzo Lea**  
Proyecto desarrollado como parte del **Reto de Ciencia de Datos – Alura Latam**  

© 2025 Estudio sobre Deserción de Clientes – Proyecto de Ciencia de Datos



