# churn-prediction-project
This project uses real-world customer data to predict churn probability and assign churn risk segments (Low, Medium, High) to help a SaaS company proactively identify at-risk users.

---

## 🔍 Goal

- Predict which customers are most likely to churn using ML models.
- Segment customers into risk levels (Low, Medium, High).
- Visualize patterns with an interactive Tableau dashboard.

---

## 📊 Tools & Techniques

- **Python**: pandas, sklearn, lightgbm, shap
- **EDA**: Correlations, chi-squared tests, z-tests
- **Models**: Logistic Regression, Random Forest, LightGBM
- **Evaluation**: ROC AUC, F1 Score, Threshold tuning
- **Explainability**: SHAP values
- **Visualization**: Tableau Public dashboard

---

## ✅ Final Results

| Metric                      | Logistic Regression | Random Forest | LightGBM (Selected) |
|----------------------------|---------------------|----------------|---------------------|
| ROC AUC                    | 0.8431              | 0.8145         | 0.8292              |
| Best F1 Score (Churners)   | 0.58                | 0.60           | **0.62**            |
| Recall (Churners)          | 0.53                | 0.76           | **0.81**            |
| Precision (Churners)       | **0.64**            | 0.49           | 0.50                |

> ✅ **LightGBM** was chosen as the final model for its superior balance of precision and recall.

---

## 📈 Tableau Dashboard

An interactive Tableau dashboard was created to:
- View the distribution of churn risk scores
- See breakdown by risk segments
- Explore how risk levels relate to monthly charges and tenure

![Dashboard Screenshot](images/dashboard_summary.png)

---

## 🔑 Top Predictive Features (via SHAP)

![SHAP Bar](images/shap_summary_bar.png)

---

## 💡 Business Recommendations

- Focus retention efforts on **High Risk** segment with short tenure & high monthly charges
- Encourage long-term contracts to reduce churn
- Target users without **OnlineSecurity** or **TechSupport** with upgrade offers

---

## 🚀 Next Steps

- Build a web-based churn scoring tool for account managers
- Set up automated dashboards using Tableau Cloud or Power BI
- Track model drift and refresh churn scores monthly

---

## 📎 Requirements

Install dependencies:
```bash
pip install -r requirements.txt
