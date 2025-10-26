# 💼 Salary Prediction for Company X

## 🧠 Overview
This capstone project aims to **predict the salary (Expected CTC)** to be offered to a potential employee using historical company data.  
The goal is to **minimize human bias** and ensure **salary equity** for employees with similar experience and qualifications.

---

## 🎯 Problem Statement
> Design a machine learning model that predicts the salary to be offered to an employee, using historical data, to minimize human bias and ensure salary fairness.

---

## 📊 Project Workflow

### 1. Data Understanding
- **Dataset**: [expected_ctc.csv](https://raw.githubusercontent.com/shlokshukla200/Capstone-Project/refs/heads/main/expected_ctc.csv)  
- Performed exploratory analysis of key features such as:
  - `Department`, `Role`, `Industry`, `Education`, `Experience`, etc.
- Identified numerical and categorical variables for further processing.

---

### 2. Data Cleaning
- Removed irrelevant columns: `IDX`, `Applicant_ID`
- Handled missing values:
  - **Numerical columns** → replaced with **median**
  - **Categorical columns** → replaced with **mode**
- Checked for duplicates and treated **outliers** using the **IQR (Interquartile Range)** method.

---

### 3. Exploratory Data Analysis (EDA)
- Visualized feature distributions using:
  - **Boxplots**
  - **Histplots**
  - **Violinplots**
  - **KDE plots**
- Created a **Correlation Heatmap** to identify relationships between features.
- Performed **Bivariate Analysis**:
  - `Total Experience` vs `Expected CTC`
  - `Current CTC` vs `Expected CTC`

---

### 4. Feature Engineering
- Applied **Label Encoding** to convert categorical columns to numerical format.
- Applied **Min-Max Scaling** to normalize numeric columns (excluding the target variable `Expected_CTC`).

---

### 5. Model Building
- **Algorithm Used**: XGBoost Regressor  
- **Train-Test Split**: 80% training / 20% testing  
- **Evaluation Metric**: R² Score

```python
from xgboost import XGBRegressor

model = XGBRegressor(
    objective='reg:squarederror',
    n_estimators=100,
    learning_rate=0.1,
    max_depth=5,
    random_state=42
)
model.fit(X_train, y_train)
6. Model Evaluation
R² Score: Measures model accuracy.

Residual Plot: Visualized errors between predicted and actual values.

Actual vs Predicted Plot: Compared real vs predicted Expected CTC values.
