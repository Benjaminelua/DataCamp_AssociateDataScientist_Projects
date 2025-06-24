# 🌾 Soil-Based Crop Prediction Using Multi-Class Classification

In this project, I apply machine learning to assist farmers in selecting the most suitable crop for their fields based on basic soil measurements. By identifying the most predictive soil feature, I aim to help reduce the need for costly and time-consuming testing of all soil components.

---

## 📄 Project Description

Farmers often face the challenge of deciding which crop to plant based on limited soil testing due to budget constraints. Measuring nitrogen (N), phosphorous (P), potassium (K), and pH levels is important, but it's not always feasible to analyze all. This project aims to determine which of these features is most predictive for identifying the optimal crop to plant.

The dataset `soil_measures.csv` contains observations of soil metrics and the corresponding crop that would yield best under those conditions.

---

## 🧪 Dataset Overview

- **File**: `soil_measures.csv`
- **Columns**:
  - `N`: Nitrogen content in the soil
  - `P`: Phosphorous content in the soil
  - `K`: Potassium content in the soil
  - `pH`: Soil pH value
  - `crop`: The optimal crop for the corresponding soil measurements (target variable)

Each row represents a field's soil metrics, and the crop that is best suited for cultivation under those conditions.

---

## 🛠️ Steps and Methodology

1. **Data Import & Exploration**  
   Loaded the dataset with `pandas` and reviewed basic statistics and structure.

2. **Modeling Approach**  
   - Built multiple logistic regression models using `sklearn.linear_model.LogisticRegression`, each trained on only one of the soil features (`N`, `P`, `K`, or `pH`) as input.
   - Evaluated model performance using accuracy from `sklearn.metrics`.

3. **Best Feature Selection**  
   - Identified the feature with the **highest classification accuracy**.
   - Stored the result in a dictionary named `best_predictive_feature`:
     ```python
     best_predictive_feature = {"<feature_name>": <accuracy_score>}
     ```

---

## 📦 Libraries Used

- `pandas` : for data manipulation
- `sklearn.linear_model.LogisticRegression` : for multi-class classification
- `sklearn.model_selection.train_test_split` : to split training and testing data
- `sklearn.metrics` : to evaluate model performance

---

## 🧠 Key Outcome

The project successfully identified the **single soil feature** with the strongest predictive power for crop selection. This insight allows farmers to prioritize which soil metric to measure, helping them make data-driven decisions while reducing testing costs.

