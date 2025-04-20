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

![image](https://github.com/user-attachments/assets/46e3e951-109a-4aa9-90b8-a213159ce240)

![image](https://github.com/user-attachments/assets/d68f6390-393f-49bd-80b6-634252ff1ee0)

![image](https://github.com/user-attachments/assets/fff50c97-1bae-4cc1-8d25-eeac6710c0ca)

![image](https://github.com/user-attachments/assets/38513266-7381-436a-b5d1-389828a100e1)

![image](https://github.com/user-attachments/assets/8b647f2f-4ff5-4f01-b094-b2d02ca6a18f)

### 🔹 Step 4: Class Imbalance Handling
- Used `SMOTE` to oversample minority class.

### 🔹 Step 5: Model Building
- Trained `RandomForestClassifier` as base model.
- Evaluated using Accuracy, Precision, Recall, F1 Score.

![image](https://github.com/user-attachments/assets/39410a87-4263-4a9f-952c-d4754cd32a5d)

### 🔹 Step 6: Boosting Models
- Trained `XGBoost` and `LightGBM` for better performance.

![image](https://github.com/user-attachments/assets/fe162070-493b-42ca-8db6-3477b50d6428)

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
