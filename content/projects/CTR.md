+++
title = "Predicting Online Advertising Click-Through Rates (CTR)"
draft = false
showReadingTime = false
showWordCount = false
tags = ["Machine Learning", "CTR", "NLP", "XGBoost", "TF-IDF"]
summary = "CTR prediction using structured features, TF-IDF text processing, and a weighted soft voting ensemble of ML models. Final model achieves 0.86 accuracy."
ShowToc = false

[cover]
  image = "/images/ctr1.jpg"

+++

## Overview

This project focuses on predicting whether a user will click on an online advertisement based on **demographics**, **browsing behavior**, and **ad headline text**. Accurate CTR prediction is essential for optimizing ad delivery and improving ROI for advertisers.

We applied a diverse set of machine learning models, enhanced them with **feature engineering** (timestamp decomposition, TF-IDF), and validated performance through rigorous evaluation metrics.

**Final model**: Soft voting ensemble (XGBoost, Random Forest, KNN)  
**Final accuracy**: **0.86**  
**Interpretability & generalization**: High

---

## Problem Statement

- **Task**: Predict whether a user will click on an ad (`click = 1`)
- **Dataset**: 10,000 samples, 9 predictors (demographics, ad topic, timestamp, etc.)
- **Target**: `click` (binary classification)

---

## Key Features

- **Balanced Dataset** (49% click / 51% no-click)
- **High-Cardinality Encoding**: Frequency encoding for `City`, `Country`
- **Temporal Features**: Hour of day, weekend flag
- **Text Processing**: TF-IDF on `Ad_Topic_Line` + PCA dimensionality reduction

---

## Models & Performance

| Model                | Accuracy  | F1 (Click=1) | AUC       |
| -------------------- | --------- | ------------ | --------- |
| Logistic Regression  | 0.805     | 0.790        | 0.896     |
| KNN                  | 0.814     | 0.807        | 0.879     |
| Random Forest        | 0.837     | 0.831        | 0.923     |
| SVM (RBF Kernel)     | 0.811     | 0.801        | 0.894     |
| Feedforward NN       | 0.812     | 0.803        | 0.872     |
| XGBoost              | 0.850     | 0.844        | 0.894     |
| **Ensemble (Final)** | **0.852** | **0.847**    | **0.918** |

**Ensemble Strategy**: Weighted soft voting  
(XGBoost: 0.6, Random Forest: 0.35, KNN: 0.05)

---

## Methodology

### Data Preprocessing

- Standardization for numeric fields
- Frequency encoding for categorical fields
- TF-IDF + PCA for `Ad_Topic_Line`
- Timestamp decomposition: `Hour_of_Day`, `Day_of_Month`, `IsWeekend`

### Training & Validation

- Stratified 60/20/20 split for train/val/test
- Cross-validation + GridSearch
- Metrics: Accuracy, F1, AUC, Learning Curve

---

## Key Insights

- **CTR peaks** at 8–9 PM, and on the 4th, 17th, and 27th
- Older users + higher income = more likely to click
- Text headlines provide **valuable predictive signals**

---

## Tools & Technologies

- **Python (Jupyter Notebook)**
- **Scikit-learn**, **XGBoost**, **TF-IDF**, **PCA**
- **Matplotlib**, **Seaborn** (visualization)

---

## Visualization Excerpts

<p>
  <img src="/images/ctr2.jpg" width="800" style="float: center;">
</p>

<p>
  <img src="/images/ctr3.jpg" width="1000" style="float: center;">
</p>

<p>
  <img src="/images/ctr4.jpg" width="1000" style="float: center;">
</p>

[View More Details](https://github.com/ritaliiii/Predicting-Online-Advertising-Click-Through-Rates-CTR-Using-Machine-Learning-and-NLP)
