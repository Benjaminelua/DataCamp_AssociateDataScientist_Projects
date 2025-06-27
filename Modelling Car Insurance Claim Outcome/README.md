# 🚗 Car Insurance Claim Prediction – Feature Selection Project

This project was built to assist **On the Road** car insurance in identifying a **single most predictive feature** that influences whether a customer will file a claim during their policy period. Given the company’s limited experience in deploying machine learning models, they requested a simple, interpretable solution that could help them kickstart their predictive modeling strategy.

---

## 🧾 Project Description

Insurance providers invest heavily in pricing optimization and risk estimation. In most countries, having car insurance is legally required, making this a highly competitive and data-driven industry.

For this project, I was given a dataset of policyholders along with their demographics, vehicle information, driving history, and claim records. My task was to determine **which single feature** is most predictive of whether a customer would make a claim.

Rather than building a complex model, I used individual logistic regression models for each feature to evaluate its performance in predicting the target variable: `outcome` (0 = no claim, 1 = made a claim). The goal was to find the **single feature** that provides the highest prediction accuracy.

---

## 📂 Dataset Overview

The dataset was provided as a single CSV file: `car_insurance.csv`.

| Column Name | Description |
|-------------|-------------|
| `id` | Unique client identifier |
| `age` | Age group: 0 = 16–25, 1 = 26–39, 2 = 40–64, 3 = 65+ |
| `gender` | Gender: 0 = Female, 1 = Male |
| `driving_experience` | Years of driving experience (0 = 0–9, 3 = 30+) |
| `education` | Education level: 0 = No education, 2 = University |
| `income` | Income class: 0 = Poverty, 3 = Upper class |
| `credit_score` | Credit score (0–1 scale) |
| `vehicle_ownership` | Vehicle ownership: 0 = Financed, 1 = Owned |
| `vehcile_year` | Year of vehicle registration: 0 = Before 2015, 1 = 2015+ |
| `married` | Marital status: 0 = Not married, 1 = Married |
| `children` | Number of children |
| `postal_code` | Postal code |
| `annual_mileage` | Annual driving mileage |
| `vehicle_type` | 0 = Sedan, 1 = Sports car |
| `speeding_violations` | Number of speeding tickets |
| `duis` | DUIs (Driving Under Influence) count |
| `past_accidents` | Number of past accidents |
| `outcome` | Target: 1 = Made a claim, 0 = No claim |

---

## 🎯 Objective
- Identify the **single best predictive feature** for car insurance claims.
- Evaluate each feature using a logistic regression model.
- Calculate prediction **accuracy** for each feature.
- Store the top-performing feature and its score in a DataFrame called `best_feature_df`.

---

## 🛠️ Tools & Techniques

- **Python** and **Pandas** for data wrangling
- **statsmodels.formula.api** for logistic regression modeling
- Accuracy metric for feature evaluation

---

## 🧪 Methodology

1. **Data Cleaning**
   - Handled missing values: median for numeric features, mode for categorical.
   - Dropped the `id` column as it's not predictive.

2. **Modeling**
   - Fit separate **logistic regression models** using each feature independently.
   - Predicted claim outcomes using a threshold of 0.5.
   - Calculated the **accuracy** of each model.

3. **Selection**
   - Identified the feature with the highest accuracy.
   - Stored the result in a structured DataFrame:  
     `best_feature_df = pd.DataFrame({"best_feature": [...], "best_accuracy": [...]})`

---

## 📦 Dependencies

- `pandas`
- `numpy`
- `statsmodels`


