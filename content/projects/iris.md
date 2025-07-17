+++
title = "Iris Dataset EDA"
draft = false
showReadingTime = false
showWordCount = false
tags = ["EDA", "Python", "Seaborn", "Matplotlib", "Iris Dataset"]
summary = "Exploratory Data Analysis of the classic Iris flower dataset using Python."
ShowToc = false

[cover]
  image = "/images/iris1.jpg"

+++

This project contains exploratory data analysis (EDA) on the classic **Iris dataset** using Python libraries like **pandas**, **seaborn**, and **matplotlib**.

The goal is to visualize and summarize patterns across different Iris flower species using key morphological features.

---

## Dataset Overview

- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/iris)
- **Features**:
  - Sepal length
  - Sepal width
  - Petal length
  - Petal width
  - Class (Iris-setosa, Iris-versicolor, Iris-virginica)

---

## Data Cleaning & Summary

- Merged features and target labels into a single DataFrame
- Checked for missing values → None found
- Detected and removed duplicates
- Verified data types → All consistent
- Verified class balance (~50 observations per class)

---

## Visualizations

- Pairplot of all features colored by species
- Boxplots and histograms for each feature
- Heatmap showing feature correlations
- Scatter plots highlighting petal/sepal separation between species

---

## Tools Used

- Python
- Pandas
- Seaborn
- Matplotlib
- Jupyter Notebook

---

## Key Insights

- **Petal length and width** are the strongest indicators for separating species
- **Setosa** species shows the most distinct cluster
- There is moderate overlap between **versicolor** and **virginica**

---

## Visualization Excerpts

<p>
  <img src="/images/iris1.jpg" width="800" style="float: center;">
</p>

<p>
  <img src="/images/iris2.jpg" width="1000" style="float: center;">
</p>

<p>
  <img src="/images/iris3.jpg" width="1000" style="float: center;">
</p>

[View More Details](https://github.com/ritaliiii/Iris-Dataset-EDA-Exploratory-Data-Analysis-)
