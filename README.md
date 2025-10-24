# 💼 Salary Prediction Using Random Forest — Machine Learning Capstone Project

🧠 **A complete end-to-end machine learning project that predicts employee salary (Expected CTC) using Random Forest.**  
The goal is to minimize human bias and promote fair salary decisions based on employee profiles and experience data.

---

## 🧩 Problem Statement

> **Design a predictive model that estimates the salary (Expected CTC) to be offered to an employee, based on their experience, education, and other professional attributes — ensuring salary equity and transparency.**

---

## ⚙️ Libraries Used

- 🧮 **NumPy** — numerical computation  
- 📊 **Pandas** — data analysis and manipulation  
- 🎨 **Matplotlib & Seaborn** — data visualization  
- 🤖 **Scikit-learn** — machine learning algorithms and evaluation  
- 📉 **Statsmodels** — statistical analysis (if used in EDA)  

---

## 📊 Workflow Overview

### 🔹 1. Data Loading
- Loaded the dataset (`expected_ctc.csv`) directly from GitHub.  
- Displayed info, shape, and column details.

### 🔹 2. Data Cleaning
- Dropped irrelevant columns (`IDX`, `Applicant_ID`, etc.).  
- Filled missing **numerical** values with the **median** and **categorical** with the **mode**.  
- Removed outliers using the **IQR method**.

### 🔹 3. Exploratory Data Analysis (EDA)
- 📈 **Univariate Analysis:** Countplots, KDE plots, and histograms.  
- 🔄 **Bivariate Analysis:** Correlation heatmaps, scatterplots, boxplots, violinplots, and pairplots.  
- Discovered strong relationships between experience, education, and expected CTC.

### 🔹 4. Feature Engineering
- Applied **One-Hot Encoding** to categorical features.  
- Generated a clean, numeric dataset ready for machine learning.

### 🔹 5. Model Building
- Implemented a **Random Forest Classifier** and **Regressor** (for continuous salary prediction).  
- Performed train-test split (80/20).  
- Evaluated model using **Mean Squared Error (MSE)** and **Accuracy Score**.

---

## 🤖 Model Summary

| Model Type              | Algorithm            | Metric Used         | Purpose                      |
|--------------------------|---------------------|---------------------|------------------------------|
| Random Forest Classifier | RandomForestClassifier | Accuracy Score      | Classification Testing       |
| Random Forest Regressor  | RandomForestRegressor  | Mean Squared Error  | Salary Prediction (CTC)      |

---

## 📈 Visualizations

- 🔹 Boxplots and KDE plots for outlier and distribution analysis  
- 🔹 Heatmaps to explore feature correlations  
- 🔹 Violin and scatter plots to visualize relationships  
- 🔹 Pairplots to show feature interactions holistically  

---

## 🧠 Insights

- Salary (Expected CTC) increases with **experience** and **education level**  
- **Appraisal ratings** and **current CTC** are strong predictors of expected salary  
- Outlier handling and encoding significantly improve model performance  
