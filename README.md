# Master-Thesis-Green-Customer-Segmentation-and-Retention-Analysis
Green Customer Segmentation and Retention Analysis  Do customers who buy more sustainably also stay more loyal? This project tests that common marketing assumption on a real retail dataset of 2,212 customers, using customer segmentation, a purchase-inactivity model, and explainable AI.
**Overview**
Built as part of a Master’s thesis at the University of Europe for Applied Sciences. The analysis combines:
1) RFM feature engineering (Recency, Frequency, Monetary), plus a Green Ratio feature: the share of each customer’s spending on fruit and fish, used as a spending-based proxy for green preference
2) Leakage-audited labelling: an early churn definition was found to leak information from a model feature, so the label was rebuilt as a 90-day purchase-inactivity proxy based on Recency alone
3) K-Means segmentation into five customer groups, with stability checks (random seeds, Gaussian Mixture comparison, skewness sensitivity)
4) XGBoost vs. logistic regression for modelling inactivity, with bootstrap confidence intervals on AUC
5) SHAP explainability to examine which features the model relies on
6) Statistical testing (chi-square, logistic regression, nonlinearity check, multivariate regression) of the green-spending/inactivity relationship

**Tech Stack**
Python, pandas, NumPy, scikit-learn, XGBoost, SHAP, statsmodels, SciPy, Plotly, Matplotlib. The thesis is written in LaTeX.

**Dataset**
Kaggle marketing_campaign dataset (2,240 customer records, 29 raw variables; 2,212 records after cleaning).
