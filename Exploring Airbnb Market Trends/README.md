# 🏙️ New York City Airbnb Market Analysis

This project analyzes short-term rental data in New York City by merging and processing data from multiple sources and formats. The goal is to provide meaningful insights (especially around **private room listings**) for a real estate startup exploring Airbnb trends in NYC.

---

## 📄 Project Description

Airbnb is widely used in New York City, a bustling hub for tourists and travelers. Listings can range from shared spaces to entire apartments. In this project, I analyze 2019 Airbnb data collected from three different file types:

- **CSV** (`airbnb_price.csv`)
- **Excel** (`airbnb_room_type.xlsx`)
- **TSV** (`airbnb_last_review.tsv`)

I extract meaningful insights for the real estate startup, focusing on:
- Review activity dates
- Room type distribution
- Average pricing

---

## 🧾 Dataset Overview

The data is stored in three different files located in the `data/` directory:

| File | Type | Key Columns | Description |
|------|------|-------------|-------------|
| `airbnb_price.csv` | CSV | `listing_id`, `price`, `nbhood_full` | Price and location data for Airbnb listings |
| `airbnb_room_type.xlsx` | Excel | `listing_id`, `description`, `room_type` | Room type and description for each listing |
| `airbnb_last_review.tsv` | TSV | `listing_id`, `host_name`, `last_review` | Last review date and host name |

---

## 🛠️ Project Objectives & Steps

1. **Load Data from Multiple Formats**  
   - Used `pandas` to read `.csv`, `.xlsx`, and `.tsv` files into DataFrames.
   
2. **Data Processing**  
   - Merged the datasets using the `listing_id` as the common key.
   - Identified the earliest and latest review dates from the `last_review` column.
   - Counted how many listings are **private rooms** based on the `room_type` column.
   - Calculated the **average listing price**, rounded to 2 decimal places.

3. **Output Generation**  
   - Created a single summary DataFrame named `review_dates` with the following columns:
     - `first_reviewed`: Earliest review date
     - `last_reviewed`: Most recent review date
     - `nb_private_rooms`: Number of private room listings
     - `avg_price`: Average price of listings in USD

   - The resulting DataFrame contains only **one row** summarizing these values.

---

## 📦 Libraries Used

- `pandas` – for data loading, merging, and transformation

