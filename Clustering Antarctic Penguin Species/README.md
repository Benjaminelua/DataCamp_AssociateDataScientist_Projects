# 🐧 Clustering Antarctic Penguins with Unsupervised Learning

This project explores unsupervised machine learning techniques to identify natural groupings in a dataset of penguins from Antarctica. You were tasked with supporting a research team by discovering clusters among penguins using physical measurements, since the actual species labels were unavailable.

---

## 📄 Project Description

The dataset (`penguins.csv`) contains information about various penguin characteristics but lacks labels for species. Your goal is to apply clustering techniques to uncover possible natural groupings, which could potentially correspond to species such as Adelie, Chinstrap, and Gentoo.

### 📊 Dataset Overview

- **Source**: Dr. Kristen Gorman and the Palmer Station, Antarctica LTER, part of the Long Term Ecological Research Network.
- **File**: `penguins.csv`
- **Features**:
  - `culmen_length_mm`: Length of the penguin's bill
  - `culmen_depth_mm`: Depth of the penguin's bill
  - `flipper_length_mm`: Length of the flipper in mm
  - `body_mass_g`: Penguin body mass in grams
  - `sex`: Penguin sex (non-numeric, not used in clustering)

---

## 🛠️ Steps and Methodology

1. **Data Import & Exploration**  
   Loaded the CSV file using `pandas`, examined data types, null values, and basic statistics.

2. **Preprocessing**  
   - Dropped the non-numeric `sex` column for clustering.
   - Scaled the numerical features using `StandardScaler` to standardize feature ranges.

3. **Clustering with K-Means**  
   - Applied K-Means clustering (from `sklearn.cluster`) on the scaled data.
   - Chose a reasonable number of clusters based on exploratory insights (e.g., potential 3 species).
   - Evaluated cluster centers and labels.

4. **Cluster Statistics Summary**  
   - Created a new DataFrame named `stat_penguins` that aggregates the **mean values** of each numeric feature by cluster.

---

## 📦 Libraries Used

- `pandas` – for data manipulation and analysis
- `matplotlib.pyplot` – for optional visualizations
- `sklearn.cluster.KMeans` – for clustering
- `sklearn.preprocessing.StandardScaler` – for standardizing features

---

## 🧠 Outcome

- The clustering revealed distinguishable groups in the penguin population using only physical features.
- The resulting `stat_penguins` DataFrame summarizes cluster-wise averages, offering insights into how penguins can be grouped even without labeled species data.


