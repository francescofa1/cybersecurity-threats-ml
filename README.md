# cybersecurity-threats-ml

# Cybersecurity Threats 2015–2024: ML Analysis & Risk Forecasting

This project explores a synthetic dataset of global cybersecurity incidents from 2015 to 2024.  
It combines data exploration, statistical analysis, and machine learning modeling to understand and predict the impact of cyber attacks.

---

## Objectives

- Explore patterns in financial loss, affected users, and resolution time.
- Analyze the influence of attack types, industries, and vulnerabilities.
- Predict:
  - Financial Loss (in Million $)
  - Incident Resolution Time (in Hours)
- Identify top predictive features and build interpretable ML models.
- Compare algorithms (Linear Regression, Lasso, XGBoost) using cross-validation.

---

## Dataset Overview

- **Rows:** 3000 incidents  
- **Columns:** 
  - Categorical: Country, Attack Type, Target Industry, Attack Source, etc.
  - Numerical: Year, Financial Loss, Affected Users, Resolution Time

---

## Techniques Used

| Step                      | Tools & Methods                        |
|---------------------------|----------------------------------------|
| Data Preprocessing        | One-hot encoding, scaling              |
| Exploratory Analysis      | Boxplots, heatmaps, violin plots       |
| Statistical Testing       | ANOVA, Kruskal-Wallis, Tukey HSD       |
| Correlation Analysis      | Pearson, Spearman                      |
| Feature Selection         | Lasso, XGBoost Feature Importance      |
| Modeling                  | Linear Regression, LassoCV, XGBoost    |
| Validation                | 5-Fold Cross-Validation (R², MAE, RMSE)|
| Visualization             | Residual plots, predictions vs actuals |

---

## Model Results (R² - Cross Validation)

| Target                | Best Model   | R² Score |
|----------------------|--------------|----------|
| Financial Loss        | XGBoost      | ~0.52    |
| Resolution Time       | LassoCV/XGBoost | ~0.22 |

A full comparison of all models and metrics is available in the notebook.

---

## Files Included

- `cybersecurity_analysis.ipynb` — main notebook (exploration and modeling)
- `README.md` — this file

---

## Key Insights

- Ransomware and Zero-day attacks are associated with the highest financial loss.
- AI-based defenses and encryption are linked to faster resolution times.
- A small number of features (top 10) can explain a significant portion of the variance.
- XGBoost outperforms linear models in both prediction tasks.

---

## Next Steps

- Hyperparameter tuning (e.g., GridSearchCV)
- Time-series modeling or forecasting
- Deploying as a dashboard or lightweight API


