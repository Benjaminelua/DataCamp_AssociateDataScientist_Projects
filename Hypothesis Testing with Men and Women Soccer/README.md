# ⚽ Investigating Goal Scoring Patterns in International Soccer: Are Women’s Matches More Goal-Intensive?

## 🧠 Project Background

As a data analyst with a passion for sports journalism, I've always been intrigued by the dynamics of soccer across different levels and divisions. After years of watching both **men’s and women’s international soccer**, I developed a strong hunch: **women’s matches tend to have more goals** than men's. But as any good analyst knows, data must speak louder than intuition.

So, I embarked on a data-driven investigation to answer a simple yet compelling question:

> **Are more goals scored in women’s international soccer matches than in men’s?**

To ensure the analysis was fair, modern, and comparable, I focused **exclusively on official FIFA World Cup matches from January 1, 2002, onward**, filtering out qualifiers and friendly games. This timeframe reflects the evolution of international football while controlling for tournament-level variance.

---

## 🎯 Objective

My goal was to perform a statistically sound hypothesis test that would either confirm or refute the assumption that **women's international matches yield more goals than men's**.

---

## 📂 Dataset Overview

The data was sourced from a reliable football statistics repository and stored in two CSV files:

- `women_results.csv`: Results of all women’s international matches from the late 19th century to present.
- `men_results.csv`: Equivalent data for men’s international matches.

Both datasets contain key attributes including:
- `date`: Match date
- `tournament`: Tournament name
- `home_score`: Home team score
- `away_score`: Away team score

---

## ❓ Hypothesis Setup

I formulated the following statistical hypotheses to guide my test, working at a **10% significance level (α = 0.10)**:

- **Null Hypothesis (H₀):** The mean number of goals scored in women's international soccer matches is the same as in men's.
- **Alternative Hypothesis (H₁):** The mean number of goals scored in women's international soccer matches is **greater** than in men's.

Given that I expected higher goal counts in women's matches, a **one-tailed test** was the appropriate choice.

---

## 🛠️ Methodology

### 1. **Data Cleaning & Filtering**
Using `pandas`, I filtered both datasets to include:
- Only **FIFA World Cup** matches.
- Only those played from **January 1, 2002** onward.

### 2. **Goal Calculation**
For each match, I computed the **total goals** by summing `home_score` and `away_score`.

### 3. **Statistical Testing**
I used a **Mann-Whitney U Test** from `scipy.stats`:
- This non-parametric test is ideal when comparing two independent samples that may not be normally distributed.
- It evaluates whether one distribution tends to have larger values than the other.
- The `alternative='greater'` parameter was used to test whether women’s matches have higher goal counts.

### 4. **Result Interpretation**
I interpreted the p-value as follows:
- If **p < 0.10**, I **reject** the null hypothesis.
- Otherwise, I **fail to reject** the null hypothesis.

### 5. **Result Format**
To keep things concise and programmatic, I stored the output in a dictionary:

```python
result_dict = {
    "p_val": p_val,
    "result": "reject" or "fail to reject"
}

