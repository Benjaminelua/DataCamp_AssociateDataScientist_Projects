# 🎬 Investigating Netflix Movies from the 1990s

## 🧠 Project Overview

As a data analyst working with a production company that specializes in **nostalgic and retro content**, I was tasked with analyzing Netflix's vast content library—specifically focusing on **movies released during the 1990s**. The goal? To better understand trends in movie length and genre during this pivotal entertainment decade, helping our team identify patterns that could influence new creative projects inspired by the '90s.

Netflix, originally founded in 1997 as a DVD rental service, has since become one of the largest streaming platforms in the world. With such an expansive catalog of shows and movies, it presents the perfect dataset for **exploratory data analysis (EDA)**.

---

## 🎯 Project Objectives

The objectives for this analysis were as follows:

1. **Explore** Netflix's movie data from the 1990s.
2. **Identify** the most frequent movie duration during the decade.
3. **Count** how many *short action movies* (under 90 minutes) were released in that period.

These insights can help our production company reimagine 90s-style content, particularly when planning movie runtimes and genre focus.

---

## 📁 Dataset Description

The dataset used for this analysis is `netflix_data.csv`. It includes detailed metadata about all Netflix shows and movies available up to the time of data collection.

### 🔍 Key Columns

| Column Name   | Description                              |
|---------------|------------------------------------------|
| `show_id`     | Unique ID of the show/movie              |
| `type`        | "Movie" or "TV Show"                     |
| `title`       | Title of the show                        |
| `director`    | Director(s) of the show                  |
| `cast`        | Cast members                             |
| `country`     | Country of origin                        |
| `date_added`  | Date added to Netflix                    |
| `release_year`| Year of release                          |
| `duration`    | Duration in minutes                      |
| `description` | Short description of the show/movie      |
| `genre`       | Genre classification (e.g., Action, Drama)|

---

## 🛠️ Tools Used

- **Python**
- **Pandas** (for data wrangling and analysis)
- **Matplotlib** (optional for visualization)

---

## 🔍 Methodology

### Step 1: Load the Dataset
I began by loading `netflix_data.csv` into a pandas DataFrame.

### Step 2: Filter for the 1990s
I selected all rows where:
- `type` was "Movie"
- `release_year` was between **1990 and 1999**

### Step 3: Clean Duration Column
To perform numeric analysis, I converted the `duration` column from string to integer.

### Step 4: Identify Most Frequent Duration
I used the `.mode()` function to find the **most common duration** for 90s movies.

### Step 5: Count Short Action Movies
I filtered the dataset again for:
- Genre = **Action**
- Duration < 90 minutes

I then calculated how many such short action films were made.

---

## 📊 Results

```python
# Example output
The most frequent movie duration is 90 minutes
The number of short action movies is 7

