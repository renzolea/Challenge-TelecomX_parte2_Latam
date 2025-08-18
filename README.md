# Telecom X – Predicción de Cancelación de Clientes (Churn)

---

## 💡 Acerca del desafío

Telecom X enfrenta una alta tasa de cancelación de clientes y busca anticipar qué clientes tienen mayor probabilidad de cancelar sus servicios. Como parte del equipo de Machine Learning, tu misión es construir un pipeline robusto que permita predecir la cancelación (churn) con alta precisión.

---

## 🎯 Objetivos del proyecto

- Preparar y preprocesar los datos para modelado.
- Realizar análisis exploratorio y selección de variables relevantes.
- Construir y entrenar modelos predictivos de clasificación.
- Evaluar el rendimiento de los modelos con métricas adecuadas.
- Interpretar los resultados y extraer insights estratégicos.
- Proponer acciones basadas en los factores que influyen en la cancelación.

---

## 🧰 Preparación de los datos

- Se utilizó un archivo CSV previamente limpiado y normalizado, con columnas relevantes.
- Se eliminaron columnas irrelevantes como identificadores únicos (`customerID`) y columnas redundantes (`account.Charges.Total`).
- Se codificaron variables categóricas mediante **One-Hot Encoding** para variables con múltiples categorías y binarización para variables binarias.
- Se verificó la proporción de clientes que cancelaron (`Churn`) para evaluar posibles desbalances.
- Se recomendó aplicar técnicas de balanceo como **SMOTE** en caso de desbalance importante.
- Se consideró la normalización de variables para modelos sensibles a escala (Regresión Logística, KNN), pero no para modelos basados en árboles.

---

## 🔎 Análisis exploratorio y selección de variables

- Se visualizó la matriz de correlación para identificar relaciones significativas con la variable objetivo (`Churn`).
- Se investigaron variables específicas como **Tiempo de contrato** y **Gasto mensual** en relación a la cancelación, usando gráficos como boxplots y scatter plots.
- Se seleccionaron variables con mayor relevancia para alimentar los modelos predictivos.

---

## 🤖 Modelado predictivo

- Se dividió el conjunto de datos en entrenamiento y prueba con una proporción de 70%-30%.
- Se entrenaron al menos dos modelos distintos para comparar desempeño:
  - **Árbol de Decisión**
  - **Random Forest**
- Se consideró la normalización para modelos sensibles y no para modelos basados en árboles.
- Se evaluó el rendimiento con métricas:
  - Exactitud (Accuracy)
  - Precisión
  - Recall
  - F1-score
  - Matriz de confusión

---

## 📊 Resultados y evaluación

| Modelo             | Exactitud | Precisión | Recall | F1-score |  
|--------------------|-----------|-----------|--------|----------|  
| Árbol de Decisión   | 72.60%    | 48.44%    | 49.91% | 49.17%   |  
| Random Forest       | 78.04%    | 60.71%    | 49.02% | 54.24%   |

- El **Random Forest** mostró mejor desempeño general, especialmente en precisión y exactitud.
- Ambos modelos presentan un recall moderado, indicando oportunidad para mejorar la detección de clientes que realmente cancelan.
- Se identificaron posibles casos de underfitting en el árbol de decisión, y se sugirieron ajustes para mejorar ambos modelos.

---

## 📈 Importancia de las variables

- Las variables más influyentes para predecir la cancelación son:
  - **Tenure (tiempo como cliente)**
  - **Tipo de contrato (ej. mensual, anual)**
  - **Cargos mensuales**
  - **Tipo de servicio de internet**
  - **Facturación sin papel**
- Estas variables fueron identificadas mediante la importancia calculada por los modelos, especialmente Random Forest.
- Su comprensión permite tomar decisiones estratégicas para mitigar la cancelación.

---

## 💡 Conclusiones y recomendaciones estratégicas

- Focalizar campañas de retención en clientes nuevos o con contratos mes a mes.
- Ofrecer incentivos para contratación anual o bianual, mejorando la fidelización.
- Revisar y ajustar planes de precios para mejorar la percepción de valor y reducir cancelaciones por costos.
- Personalizar la experiencia según el tipo de servicio contratado, mejorando la satisfacción.
- Promover la facturación digital y comunicación proactiva para fortalecer el vínculo con el cliente.

---

## 📚 Recursos y referencias

- Artículo sobre codificación categórica: [Alura](https://www.alura.com.br/artigos/codificacao-categorica)
- Manejo del desbalanceo de clases: [Alura](https://www.alura.com.br/artigos/lidando-com-desbalanceamento-dados)
- Normalización y estandarización en Machine Learning: [Medium](https://medium.com/ipnet-growth-partner/padronizacao-normalizacao-dados-machine-learning-f8f29246c12)

---

## Contacto

Si querés colaborar o tenés dudas sobre este proyecto, no dudes en contactarme.

---

## 🛡️ Insignia

La realización y entrega de este proyecto otorgó una exclusiva insignia:

![Badge Challenge TelecomX Analisis Evasión Clientes - Alura](https://cdn1.gnarususercontent.com.br/6/409126/832d01c5-aa1f-4a72-894b-9bb18b8d2a00.png)

---
¡Gracias por tu interés en el análisis de cancelación de Telecom X!


