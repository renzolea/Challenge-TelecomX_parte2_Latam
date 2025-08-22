# ⭐️ Project: Customer Churn Analysis at Telecom X  

⭐️ **Overview**  
This project analyzes customer churn at Telecom X, aiming to predict which users are most likely to leave the service. Through data cleaning, exploratory analysis, and predictive modeling, the goal is to derive strategic insights to improve customer retention.  

⭐️ **Project Files**  
- `TelecomX_LATAM.ipynb` → Notebook containing the full analysis.  
- `Dataset.csv` → Preprocessed data.  
- `README.md` → Explanatory documentation.  

⭐️ **Tools and Libraries**  
- Python 3.x  
- Pandas, NumPy  
- Matplotlib, Seaborn, Plotly  
- Scikit-learn  
- Jupyter Notebook  

⭐️ **Environment Setup**  
```bash
git clone https://github.com/renzolea/TelecomX-Churn-Analysis
pip install pandas numpy matplotlib seaborn plotly scikit-learn
jupyter notebook TelecomX_LATAM.ipynb
⭐️ Methodological Workflow

- Data cleaning and preparation.
- Conduct exploratory data analysis with visualizations.
- Split dataset into training (70%) and testing (30%).
- Build predictive models: Decision Tree and Random Forest.
- Evaluate models using Accuracy, Precision, Recall, F1-score, and confusion matrix.
- Identify the most influential features for churn prediction.

⭐️ Comparative Results

| Model           | Accuracy | Precision | Recall  | F1-score |
|-----------------|----------|-----------|---------|----------|
| Decision Tree   | 72.41%   | 48.06%    | 48.66%  | 0.4836   |
| Random Forest   | 78.32%   | 61.17%    | 50.27%  | 0.5519   |

⭐️ Results Interpretation

- Random Forest outperforms the Decision Tree in Accuracy, Precision, and F1-score, reducing errors when predicting churn.
- Recall for both models is approximately 50%, showing room for improvement in capturing all actual churned customers.

⭐️ Overfitting / Underfitting

- **Decision Tree**: Performance limited (72% Accuracy), likely underfitting due to oversimplified structure.
  - 🔧 Recommendation: adjust `max_depth` between 5–10, increase `min_samples_split` and `min_samples_leaf`.
- **Random Forest**: Better generalization (78% Accuracy), though low Recall indicates bias toward the majority class (non-churn).
  - 🔧 Recommendation: use `class_weight="balanced"`, increase `n_estimators` (≥300), tune `max_depth` and `max_features`, and optimize using GridSearchCV.

⭐️ Most Influential Variables

- Customer tenure (Tenure)
- Contract type
- Monthly charges
- Payment method
- Internet service type

⭐️ Conclusions and Strategic Recommendations

- Random Forest is the most robust model for churn prediction, offering a balance between Accuracy and Precision while maintaining detection ability.
- High-risk customers: those with monthly contracts, low tenure, and high monthly charges.
- Recommended retention strategies: early loyalty programs, incentives for long-term contracts, pricing adjustments, and personalized service experiences.

⭐️ Authorship

Project developed by **Renzo Lea** as part of the Alura Latam Data Science challenge.

© 2025 – Customer Churn Analysis – Data Science Project
