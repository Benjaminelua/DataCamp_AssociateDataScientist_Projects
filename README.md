# 🧪 DataCamp Projects Portfolio

This repository contains a collection of 10 practical associate Data Scientist projects completed through DataCamp's Associoate Data Scientist Track. These projects demonstrate key skills in Python, data wrangling, machine learning, hypothesis testing, data visualization, and more. Each project is independent and includes problem statements, datasets, and solutions in Jupyter Notebook format.

---

## 📁 Project List

### [1. Investigating Netflix Movies](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Investigating%20Netflix%20Movies)
The objectives for this analysis were as follows:

1. **Explore** Netflix's movie data from the 1990s.
2. **Identify** the most frequent movie duration during the decade.
3. **Count** how many *short action movies* (under 90 minutes) were released in that period.

These insights can help our production company reimagine 90s-style content, particularly when planning movie runtimes and genre focus.

---

### [2.Clustering Antarctic Penguin with Unsupervised Learning](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Clustering%20Antarctic%20Penguin%20Species)
This project explores unsupervised machine learning techniques to identify natural groupings in a dataset of penguins from Antarctica. I was tasked with supporting a research team by discovering clusters among penguins using physical measurements, since the actual species labels were unavailable.

---

### [3. Exploring Airbnb Market Trends](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Exploring%20Airbnb%20Market%20Trends)
Airbnb is widely used in New York City, a bustling hub for tourists and travelers. Listings can range from shared spaces to entire apartments. In this project, I analyze 2019 Airbnb data collected from three different file types:

- **CSV** (`airbnb_price.csv`)
- **Excel** (`airbnb_room_type.xlsx`)
- **TSV** (`airbnb_last_review.tsv`)

I extract meaningful insights for the real estate startup, focusing on:
- Review activity dates
- Room type distribution
- Average pricing
  
---

### [4. Exploring NYC Public School Results](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Exploring%20NYC%20Public%20School%20Test%20Results)
Analyzing SAT results provides valuable insights for education policymakers, researchers, city officials, and parents evaluating school quality. I was tasked with exploring school performance in math, identifying top-performing schools overall, and determining the borough with the most variation in SAT scores.

Using the `schools.csv` dataset, I answered three key questions:
1. **Which NYC schools have the best math results?**
2. **What are the top 10 performing schools based on total SAT scores?**
3. **Which borough has the largest standard deviation in SAT performance?**

---

### [5. Hypothesis Test with Men and Women Soccer](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Hypothesis%20Testing%20with%20Men%20and%20Women%20Soccer)
As a data analyst with a passion for sports journalism, I've always been intrigued by the dynamics of soccer across different levels and divisions. After years of watching both **men’s and women’s international soccer**, I developed a strong hunch: **women’s matches tend to have more goals** than men's. But as any good analyst knows, data must speak louder than intuition.

So, I embarked on a data-driven investigation to answer a simple yet compelling question:

> **Are more goals scored in women’s international soccer matches than in men’s?**

To ensure the analysis was fair, modern, and comparable, I focused **exclusively on official FIFA World Cup matches from January 1, 2002, onward**, filtering out qualifiers and friendly games. This timeframe reflects the evolution of international football while controlling for tournament-level variance.

---

### [6. Modelling Car Insurance Claim Outcome](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Modelling%20Car%20Insurance%20Claim%20Outcome)
Insurance providers invest heavily in pricing optimization and risk estimation. In most countries, having car insurance is legally required, making this a highly competitive and data-driven industry.
For this project, I was given a dataset of policyholders along with their demographics, vehicle information, driving history, and claim records. My task was to determine **which single feature** is most predictive of whether a customer would make a claim.
Rather than building a complex model, I used individual logistic regression models for each feature to evaluate its performance in predicting the target variable: `outcome` (0 = no claim, 1 = made a claim). The goal was to find the **single feature** that provides the highest prediction accuracy.

---

### [7. Predicting DVD Rental Duration](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Predicting%20DVD%20Rental%20Duration)
This project involves building a machine learning model to predict how many days a customer will rent a DVD from a movie rental company. Accurate predictions help the company optimize inventory management and reduce operational inefficiencies. The goal was to develop a regression model with a **Mean Squared Error (MSE) less than 3** on the test dataset.

---

### [8. Predictive Modelling for Agriculture](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Predictive%20Modelling%20for%20Agriculture)
Farmers often face the challenge of deciding which crop to plant based on limited soil testing due to budget constraints. Measuring nitrogen (N), phosphorous (P), potassium (K), and pH levels is important, but it's not always feasible to analyze all. This project aims to determine which of these features is most predictive for identifying the optimal crop to plant.

The dataset `soil_measures.csv` contains observations of soil metrics and the corresponding crop that would yield best under those conditions.


---

### [9. Preparing Data for Modelling](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Preparing%20Data%20for%20Modelling)
This project focused on transforming a large customer dataset from **Training Data Ltd.**, a leading online data science training provider. The objective was to build a **memory-efficient version** of their student data for predictive modeling, specifically to identify students likely to seek new job opportunities.

Large datasets often introduce performance challenges during training and inference. This project demonstrated that by applying proper data type conversions and targeted filtering, **significant memory reduction** can be achieved without sacrificing data integrity.

---

### [10. Visualizing Nobel Price Winner](https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects/tree/main/Visualizing%20Nobel%20Price%20Winners)
The **Nobel Prize** stands as one of the most prestigious international honors, recognizing outstanding contributions to humanity in fields like **Physics, Chemistry, Medicine, Literature, Peace**, and **Economics**. Since its inception in **1901**, hundreds of remarkable individuals and organizations have been celebrated for their achievements.

In this project, I performed a historical analysis of Nobel Prize winners from **1901 to 2023** using data obtained from the **Nobel Prize API**. The dataset includes details about each laureate, including their gender, birth country, prize category, and the year of their award. The main objective was to uncover interesting trends and patterns across decades, regions, and demographics.

---

## 🧰 Tools and Technologies

- **Languages**: Python
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`
- **Techniques**: Data Cleaning, Exploratory Data Analysis, A/B Testing, Hypothesis Testing, Classification, Feature Engineering, Data Merging, Visualization

---

## 📌 How to Use

Each project folder contains:
- A `.ipynb` Jupyter Notebook with explanations and code.
- Input datasets (if not large or proprietary).

### ▶️ Run Locally

```bash
# Clone the repository
git clone https://github.com/Benjaminelua/DataCamp_AssociateDataScientist_Projects.git

# Open Jupyter Notebook
jupyter notebook
```

---

## 👨‍💻 Author

**Benjamin Patrick**  
🎓 Associate Data Sceintist | 📊 Python Developer | 🧠 Lifelong Learner  
Connect with me on [LinkedIn](www.linkedin.com/in/patrick-benjamin-a0b524267) • [GitHub](https://github.com/Benjaminelua)

---

## 📄 License

This repository is licensed under the **MIT License**. See [LICENSE](./LICENSE) for details.



