# 🏦 Loan Prediction Case Study

## 🎯 Objective
Build a machine learning model to predict whether a loan will be approved based on applicant and loan-related information.

This project demonstrates an end-to-end data science workflow including:
- Data cleaning
- Feature engineering
- Exploratory Data Analysis (EDA)
- Model training & evaluation
- Handling class imbalance
- Trying advanced boosting models

---

## 🧾 Dataset
The dataset is located in the [`data/`](./data) folder and includes:

- Gender, Marital Status, Dependents
- Education, Self-Employment status
- ApplicantIncome, CoapplicantIncome
- LoanAmount, Loan_Amount_Term
- Credit History
- Property Area
- Loan Status (Target Variable)

> `Loan_Status = Y` means approved, `N` means not approved.

---

## 📊 Workflow

### 🔹 Step 1: Data Cleaning
- Handle missing values using mode (categorical) and median (numerical).

### 🔹 Step 2: Feature Engineering
- Encoded categorical variables.
- Created new features: `Total_Income`, `Debt_To_Income`, `Income_Per_Person`.

### 🔹 Step 3: EDA
- Visualized loan approvals by income, loan amount, and property area.
- Checked correlations between variables.

### 🔹 Step 4: Class Imbalance Handling
- Used `SMOTE` to oversample minority class.

### 🔹 Step 5: Model Building
- Trained `RandomForestClassifier` as base model.
- Evaluated using Accuracy, Precision, Recall, F1 Score.

### 🔹 Step 6: Boosting Models
- Trained `XGBoost` and `LightGBM` for better performance.

---

## ✅ Results

| Model          | Accuracy |
|----------------|----------|
| Random Forest  | ~80-85%  |
| XGBoost        | ~85-87%  |
| LightGBM       | ~85-87%  |

> Metrics may vary depending on random seed and data splits.

---

## 🚀 Improvements & Extensions
- Hyperparameter tuning (`GridSearchCV`)
- Model calibration for better probability estimation
- Stacking/blending multiple models
- Feature selection with SHAP or permutation importance
- Deployment with Streamlit or Flask (future scope)

---

## 🗃️ Repository Structure

```
📦 loan-prediction-case-study/
├── data/
│   └── train_loan_pred.csv
├── requirements.txt
├── Loan_Prediction_Case_Study.ipynb
├── README.md
```