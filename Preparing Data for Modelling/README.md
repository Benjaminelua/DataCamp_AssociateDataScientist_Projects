# 🚀 Efficient Dataset Transformation for Predictive Modeling

## 📌 Project Overview

This project focused on transforming a large customer dataset from **Training Data Ltd.**, a leading online data science training provider. The objective was to build a **memory-efficient version** of their student data for predictive modeling, specifically to identify students likely to seek new job opportunities.

Large datasets often introduce performance challenges during training and inference. This project demonstrated that by applying proper data type conversions and targeted filtering, **significant memory reduction** can be achieved without sacrificing data integrity.

---

## 📂 Dataset Description

The dataset, `customer_train.csv`, contains anonymized student records and a label indicating if each student is looking for a new job.

### 🔑 Key Columns

| Column Name             | Description                                                   |
|-------------------------|---------------------------------------------------------------|
| `student_id`            | Unique identifier for each student                            |
| `city`                  | Encoded city location                                         |
| `city_development_index` | Scaled index indicating city development                    |
| `gender`                | Gender of the student                                         |
| `relevant_experience`  | Whether the student has relevant work experience              |
| `enrolled_university`  | University enrollment status                                  |
| `education_level`       | Highest level of education attained                          |
| `major_discipline`     | Field of study                                                 |
| `experience`           | Total work experience in years                                 |
| `company_size`         | Number of employees at current company                         |
| `company_type`         | Type of company employing the student                          |
| `last_new_job`         | Years since the last job change                                |
| `training_hours`       | Number of training hours completed                             |
| `job_change`           | Binary label: 1 if seeking a new job, else 0                  |

---

## 🎯 Objective

To transform the dataset for:

- ✅ Efficient storage and memory usage  
- ✅ Effective filtering for modeling relevance  
- ✅ Preservation of important categorical and ordinal relationships

---

## 🛠️ Transformations Applied

### ✅ Filtering

Focused the dataset on enterprise-relevant professionals by keeping:

- Students with **≥ 10 years** of experience
- Employed at companies with **≥ 1000 employees**

### ✅ Data Type Optimization

| Transformation        | Description |
|-----------------------|-------------|
| **Booleans**          | Binary columns like `gender`, `relevant_experience`, and `job_change` stored as `bool` |
| **Integers**          | Columns like `student_id`, `training_hours` converted to `int32` |
| **Floats**            | `city_development_index` converted to `float16` |
| **Nominal Categories**| Columns like `city`, `major_discipline`, `company_type` stored as `category` |
| **Ordinal Categories**| Ordered columns (`experience`, `company_size`, `education_level`, `enrolled_university`, `last_new_job`) converted using `CategoricalDtype` with custom-defined orders |

---

## 📈 Example: Custom Categorical Ordering

```python
from pandas.api.types import CategoricalDtype

# Define experience order
experience_order = [str(i) for i in range(1, 21)] + [">21"]
experience_dtype = CategoricalDtype(categories=experience_order, ordered=True)

# Apply to column
ds_jobs_transformed['experience'] = ds_jobs_transformed['experience'].astype(experience_dtype)
```

---

## 🧾 Files Included

- `customer_train.csv` – Original dataset (**not included here**)  
- `transform_ds_jobs.py` – Python script containing the full transformation pipeline

---

## 🧠 Key Takeaways

- ✔️ Proper data type conversion can **drastically improve memory usage**
- ✔️ Storing ordinal variables with a natural order enhances **model performance**
- ✔️ Domain-relevant filtering increases **predictive power** and **business alignment**


