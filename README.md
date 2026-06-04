# 🏥 Insurance Pricing Risk Prediction System

This project builds a machine learning system to predict medical insurance charges and generate risk-based insurance premiums. It simulates a real-world actuarial pricing model used in the insurance industry.

---

# 📊 Project Overview

The goal of this project is to analyze customer health and demographic data and build predictive models that estimate insurance costs.

We go beyond prediction by transforming outputs into a **pricing engine**, which can be used to support insurance underwriting decisions.

---

# 🎯 Objectives

- Predict medical insurance charges using machine learning
- Identify key risk factors affecting insurance costs
- Compare Linear Regression vs XGBoost models
- Improve performance using hyperparameter tuning
- Build a risk-based pricing framework

---

# 📁 Dataset

- Source: Kaggle Medical Insurance Dataset
- Features:
  - Age
  - Sex
  - BMI
  - Number of children
  - Smoking status
  - Region
- Target:
  - Insurance charges

---

# 🧠 Methodology

## 1. Data Preprocessing
- Handling categorical variables (sex, smoker, region)
- Feature engineering:
  - BMI interactions
  - Family size
  - Risk indicators

---

## 2. Exploratory Data Analysis (EDA)
- Distribution of insurance charges
- Relationship between BMI, age, smoking, and charges
- Correlation analysis

Key insight:
- Smoking status is the strongest predictor of insurance cost.

---

## 3. Feature Engineering
- One-hot encoding for categorical variables
- Interaction features:
  - smoker × BMI
  - age groups
- Risk-based transformations

---

## 4. Machine Learning Models

### Models Used:
- Linear Regression (baseline model)
- XGBoost Regressor (advanced model)
- Tuned XGBoost (optimized model)

---

## 5. Hyperparameter Tuning
- Grid Search Cross Validation
- Optimized:
  - n_estimators
  - max_depth
  - learning_rate
  - subsample

---

# 📈 Model Performance

| Model | MAE | RMSE | R² |
|------|------|------|------|
| Linear Regression | 2837.29 | 4575.55 | 0.8861 |
| XGBoost | 2458.45 | 4324.98 | 0.8982 |
| Tuned XGBoost | 2463.82 | 4286.18 | 0.9000 |

---

# 🏆 Best Model

✔ **Tuned XGBoost Regressor**

Reason:
- Highest R² score
- Lowest RMSE
- Best overall generalization performance

---

# 🔍 Feature Importance Insights

Most influential factors affecting insurance charges:

1. 🚬 Smoking status (strongest impact)
2. 🎂 Age
3. ⚖️ BMI
4. 👨‍👩‍👧 Family size (moderate effect)
5. 🌍 Region (low impact)
6. ⚧ Gender (minimal impact)

---

# 💡 Business Insights

- Smokers generate significantly higher insurance costs → highest risk group
- Age and BMI increase medical risk linearly and non-linearly
- Gender and region have limited predictive power
- Risk-based pricing models can significantly improve premium accuracy

---

# 🧾 Insurance Pricing Logic

Final pricing formula used:

```
Premium = Predicted Medical Cost × Risk Loading Factor (1.2)
```

This simulates real-world insurance pricing strategies.

---

# 🛠️ Tech Stack

- Python 🐍
- Pandas / NumPy
- Scikit-learn
- XGBoost
- Matplotlib / Seaborn
- Flask (optional deployment layer)
- Jupyter Notebook

---

# 📊 Project Structure

```
insurance-pricing-project/
│
├── data/
├── notebooks/
│   ├── EDA.ipynb
│   ├── modeling.ipynb
│
├── models/
│   ├── xgboost_model.pkl
│
├── reports/
│   ├── figures/
│
├── README.md
```

---

# 🚀 Future Improvements

- Deploy model using Flask / FastAPI
- Add SHAP explainability for predictions
- Build interactive dashboard (Power BI / Streamlit)
- Add real-time insurance quote system
- Integrate with cloud deployment (AWS / Render)

---

# 👨‍💻 Author

Developed as a Data Science portfolio project focusing on:
- Machine Learning
- Insurance Risk Modeling
- Predictive Analytics
- Real-world pricing systems

---

# 📌 Key Takeaway

This project demonstrates how machine learning can be used not only for prediction but also for **decision-making in financial pricing systems**, similar to real actuarial models used in insurance companies.
