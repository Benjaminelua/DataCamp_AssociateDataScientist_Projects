# 🏅 Visualizing the History of Nobel Prize Winners (1901–2023)

## 📚 Project Overview

The **Nobel Prize** stands as one of the most prestigious international honors, recognizing outstanding contributions to humanity in fields like **Physics, Chemistry, Medicine, Literature, Peace**, and **Economics**. Since its inception in **1901**, hundreds of remarkable individuals and organizations have been celebrated for their achievements.

In this project, I performed a historical analysis of Nobel Prize winners from **1901 to 2023** using data obtained from the **Nobel Prize API**. The dataset includes details about each laureate, including their gender, birth country, prize category, and the year of their award. The main objective was to uncover interesting trends and patterns across decades, regions, and demographics.

---

## 🎯 Key Objectives

This project focused on answering the following data-driven questions:

1. 🧑‍🤝‍🧑 What is the most commonly awarded **gender** and **birth country**?
2. 🇺🇸 Which **decade** had the highest **ratio of US-born winners** compared to total winners?
3. 👩‍🔬 What **decade-category combination** had the highest proportion of **female laureates**?
4. 👩 Who was the **first woman** to receive a Nobel Prize, and in which category?
5. 🔁 Who are the **individuals or organizations** that have won **multiple Nobel Prizes**?

---

## 🗂️ Dataset Information

- **Filename:** `nobel.csv`
- **Source:** Nobel Prize API (https://nobelprize.org)
- **Location:** `data/` folder

### Key Columns

| Column Name     | Description                                     |
|------------------|-------------------------------------------------|
| `year`           | Year the prize was awarded                     |
| `category`       | Prize category (e.g., Physics, Peace)          |
| `full_name`      | Full name of the laureate or organization      |
| `birth_country`  | Country of birth                               |
| `sex`            | Gender of the laureate                         |
| `organization_name` | Name of awarding organization (if any)     |

---

## 🛠️ Tools and Technologies

- **Python**  
- **Pandas** for data analysis  
- **NumPy** for numeric computation  
- **Seaborn** for visual exploration (optional)

---

## 🔍 Analytical Process

### 🏆 Most Awarded Gender and Country
We identified the **most frequent gender** and **birth country** among Nobel winners by counting occurrences in the dataset.

```python
top_gender = df["sex"].value_counts().idxmax()
top_country = df["birth_country"].value_counts().idxmax()

