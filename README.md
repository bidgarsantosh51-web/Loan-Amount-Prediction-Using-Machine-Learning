# 💰 Loan Amount Prediction Using Machine Learning

A machine-learning regression project for predicting the **loan amount** a customer may receive based on financial, employment, credit, and personal attributes.

The project covers **Exploratory Data Analysis (EDA), data preprocessing, regression modeling, model evaluation, residual analysis, and feature importance analysis** using Linear Regression and Random Forest Regressor.

---

## 📋 Table of Contents

1. [Project Overview](#-project-overview)
2. [Dataset Details](#-dataset-details)
3. [Project Workflow](#-project-workflow)
4. [Model Performance](#-model-performance)
5. [Feature Importance](#-feature-importance)
6. [Prediction Example](#-prediction-example)
7. [Technologies Used](#-technologies-used)

---

## 🔍 Project Overview

The objective of this project is to predict a suitable **loan amount** for an applicant using financial and personal information.

The models use features such as:

* Income
* Credit score
* Employment experience
* Monthly expenses
* Existing loans and EMI
* Savings
* Asset value
* Loan term
* Interest rate
* Debt-to-income ratio
* Number of dependents

This project compares a simple **Linear Regression** baseline with a **Random Forest Regressor** to understand which approach performs better on unseen data.

---

## 🗃️ Dataset Details

The dataset contains **10,000 observations** with **14 independent features** and the target variable `loan_amount`.

### Features

| Feature                | Description             |
| ---------------------- | ----------------------- |
| `age`                  | Age of the applicant    |
| `monthly_income`       | Monthly income          |
| `annual_income`        | Annual income           |
| `employment_years`     | Years of employment     |
| `credit_score`         | Creditworthiness score  |
| `monthly_expenses`     | Monthly expenses        |
| `existing_loan_amount` | Existing loan amount    |
| `existing_emi`         | Existing EMI            |
| `savings`              | Applicant savings       |
| `assets_value`         | Total asset value       |
| `loan_term_months`     | Loan duration in months |
| `interest_rate`        | Loan interest rate      |
| `debt_to_income`       | Debt-to-income ratio    |
| `dependents`           | Number of dependents    |

**Target Variable:** `loan_amount`

---

## 🛠️ Project Workflow

### 1. Exploratory Data Analysis

* Inspected the dataset structure and statistical summaries.
* Analysed the distribution of `loan_amount`.
* Examined relationships between variables using correlation analysis and visualizations.
* Investigated important financial variables related to the target.
* Analysed residuals after model development.

### 2. Data Preprocessing

* Separated input features (`X`) and target (`y`).
* Checked the dataset for data-quality issues.
* Split the dataset into **80% training and 20% testing data**.

### 3. Model Development

Two regression models were trained:

* **Linear Regression** — used as the baseline model.
* **Random Forest Regressor** — used as an ensemble-based regression model.

---

## 📈 Model Performance

The models were evaluated on unseen test data using **Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² Score**.

| Model                       |          MAE (₹) |         RMSE (₹) |   R² Score |
| --------------------------- | ---------------: | ---------------: | ---------: |
| Linear Regression           |     ₹1,40,907.85 |     ₹1,92,816.02 |     0.6910 |
| **Random Forest Regressor** | **₹1,30,831.82** | **₹1,77,653.89** | **0.7377** |

### Key Takeaway

Random Forest Regressor performed better than Linear Regression on all three evaluation metrics.

* MAE improved by approximately **₹10,076**
* RMSE decreased by approximately **₹15,162**
* R² improved from **0.6910 to 0.7377**

Based on the test results, **Random Forest Regressor was selected as the final model**.

---

## ⚡ Feature Importance

Feature importance from the Random Forest model showed the following major contributors:

| Feature            | Importance |
| ------------------ | ---------: |
| `monthly_income`   |     24.74% |
| `annual_income`    |     24.66% |
| `credit_score`     |     20.95% |
| `loan_term_months` |      6.11% |
| `employment_years` |      4.47% |
| `debt_to_income`   |      3.16% |
| `savings`          |      3.11% |

The results indicate that **income and credit score** were the most influential features for predicting loan amount in this dataset.

---

## 🚀 Prediction Example

A prediction function was created to test the trained Random Forest model on new applicant information.

Example output from the project:

**Predicted Loan Amount: ₹7,21,100 (~₹7.21 Lakh)**

This demonstrates how the trained model can be used to generate a loan amount prediction for a new set of applicant attributes.

---

## 💻 Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Google Colab**

---

## 📌 Conclusion

This project demonstrates the complete workflow of a regression-based machine-learning problem, from data exploration and preprocessing to model comparison and interpretation.

Among the evaluated models, **Random Forest Regressor achieved the best test performance with an R² score of 0.7377**, making it the preferred model for this dataset.
