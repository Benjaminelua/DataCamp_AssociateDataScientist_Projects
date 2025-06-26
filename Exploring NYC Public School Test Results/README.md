# 🎓 NYC Public School SAT Performance Analysis

In this project, I analyzed SAT performance data from New York City public high schools. The SAT is a crucial standardized exam used by colleges across the U.S. for admissions decisions. The test consists of three sections: **math**, **reading**, and **writing**, each with a maximum score of 800 points. This means a total perfect score is 2400.

Analyzing SAT results provides valuable insights for education policymakers, researchers, city officials, and parents evaluating school quality. I was tasked with exploring school performance in math, identifying top-performing schools overall, and determining the borough with the most variation in SAT scores.

---

## 🧾 Project Objectives

Using the `schools.csv` dataset, I answered three key questions:

1. **Which NYC schools have the best math results?**
2. **What are the top 10 performing schools based on total SAT scores?**
3. **Which borough has the largest standard deviation in SAT performance?**

---

## 📂 Dataset Overview

The dataset `schools.csv` contains the following relevant columns:

| Column Name       | Description                          |
|-------------------|--------------------------------------|
| `school_name`     | Name of the NYC public high school   |
| `borough`         | NYC borough where the school is located |
| `average_math`    | Average SAT math score               |
| `average_reading` | Average SAT reading score            |
| `average_writing` | Average SAT writing score            |

---

## 📈 Analysis Steps

### 🔹 1. Best Math Performing Schools

I considered any school with a math average of **at least 640** (80% of 800) as having excellent math performance.

- Filtered these schools.
- Stored results in a DataFrame called `best_math_schools`.
- Sorted the results by `average_math` in descending order.

```python
best_math_schools = schools[schools["average_math"] >= 640][["school_name", "average_math"]].sort_values(by="average_math", ascending=False)

