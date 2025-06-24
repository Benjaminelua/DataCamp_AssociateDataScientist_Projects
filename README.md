# 🎬 Predicting DVD Rental Duration

## 📌 Project Overview

This project involves building a machine learning model to predict how many days a customer will rent a DVD from a movie rental company. Accurate predictions help the company optimize inventory management and reduce operational inefficiencies. The goal was to develop a regression model with a **Mean Squared Error (MSE) less than 3** on the test dataset.

The project was completed as part of the [DataCamp Associate Data Scientist track](https://www.datacamp.com/tracks/associate-data-scientist-with-python) using Python and various data science libraries.

---

## 📊 Dataset Description

The dataset `rental_info.csv` includes the following features:

- `rental_date`: Date and time when the DVD was rented
- `return_date`: Date and time when the DVD was returned
- `amount`: Amount paid by the customer
- `amount_2`: Square of the amount
- `rental_rate`: Rate charged for the DVD
- `rental_rate_2`: Square of the rental rate
- `release_year`: Release year of the movie
- `length`: Duration of the movie in minutes
- `length_2`: Square of the length
- `replacement_cost`: Cost to replace the DVD
- `special_features`: Special features such as "Deleted Scenes" or "Behind the Scenes"
- `NC-17`, `PG`, `PG-13`, `R`: Dummy variables indicating movie ratings

The target variable `rental_length_days` was engineered using the difference between `return_date` and `rental_date`.

---

## 🧪 Project Objectives

- Perform exploratory data analysis and preprocessing
- Engineer new features (`rental_length_days`, dummy variables for `special_features`)
- Avoid data leakage when selecting model features
- Train and evaluate regression models
- Achieve an MSE ≤ 3 on the test set
- Select and save the best model as `best_model`

---

## 🛠️ Tools & Technologies Used

- **Python**
- **Pandas** for data manipulation
- **NumPy** for numerical computations
- **Scikit-learn** for machine learning

---

## 🚀 Steps Taken

1. **Data Preprocessing**  
   - Parsed datetime columns  
   - Calculated `rental_length_days`  
   - Created dummy variables from `special_features`  
   - Removed any features that could lead to data leakage

2. **Feature Selection & Modeling**  
   - Selected appropriate numerical and categorical features  
   - Split data into training and test sets (`test_size=0.2`, `random_state=9`)  
   - Trained multiple regression models  
   - Evaluated using Mean Squared Error (MSE)

3. **Model Selection**  
   - Chose the model with MSE < 3  
   - Stored it as `best_model`  
   - Stored its MSE score in `best_mse`

---

## 📈 Results

- ✅ Successfully built a regression model with **MSE below 3**
- 📌 Final model: *[Random Forest Regressor]*
- 🧮 `best_mse`: *[2.0301]*



