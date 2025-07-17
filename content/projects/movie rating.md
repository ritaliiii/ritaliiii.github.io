+++
title = "Movie Ratings, Genres & Financial Performance Analysis"
draft = false
showReadingTime = false
showWordCount = false
tags = ["Python", "EDA", "Visualization", "ROI", "Outlier Analysis"]
summary = "An analysis of 45k+ movies exploring how genres, ratings, and budgets relate to ROI and audience approval using Kaggle's Movies Dataset."
ShowToc = false

[cover]
  image = "/images/movie1.jpg"

+++

## Project Overview

This project investigates how movie ratings, genres, and budgets relate to financial performance using the `movies_metadata.csv` file from the Kaggle Movies Dataset. By analyzing ~45,000 movies, we aim to uncover insights into what drives ROI and audience approval in the film industry.

---

## Objectives

- Explore the relationship between **weighted movie ratings** and **return on investment (ROI)**
- Analyze the impact of **budget categories** and **genre** on financial performance
- Identify **trends** in ratings and revenue over time
- Detect **rating and ROI outliers** using statistical methods

---

## Tools Used

- **Python**, **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**
- **Scikit-learn** (for standardization), **SciPy**
- **Jupyter Notebook**

---

## Dataset Information

- File: `movies_metadata.csv`
- Key columns used:
  - `id`
  - `title`
  - `release_date`
  - `genres`
  - `vote_average`
  - `vote_count`
  - `budget`
  - `revenue`

---

## Data Cleaning & Preprocessing

- Converted numeric columns (`budget`, `revenue`, `vote_count`, `vote_average`) to appropriate types
- Handled missing values and removed rows with zero budget or revenue
- Parsed `genres` column from stringified lists to extract genre names

---

## Key Features Engineered

### ROI Calculation

ROI = (revenue - budget) / budget

---

## Outlier Analysis: ROI & Rating Over/Underperformers

To identify movies that significantly overperformed or underperformed in terms of ROI and audience ratings, we used Z-score standardization.

### 📈Methodology

- **Z-Score Calculation:**

  - ROI Z-score: `z = (ROI - mean) / std` using `scipy.stats.zscore`
  - Weighted Rating Z-score: same method applied to `weighted_rating`

- **Thresholds:**
  - Z-score > 2: **Overperformers**
  - Z-score < -2: **Underperformers**

---

## Visualization Excerpts

<p>
  <img src="/images/movie2.jpg" width="1000" style="float: center;">
</p>

<p>
  <img src="/images/movie3.jpg" width="1000" style="float: center;">
</p>

<p>
  <img src="/images/movie4.jpg" width="1000" style="float: center;">
</p>

[View More Details](https://github.com/ritaliiii/Movie-Ratings-Genres-Financial-Performance-Analysis)
