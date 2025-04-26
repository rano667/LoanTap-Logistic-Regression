# Loan Default Prediction Project

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1PBFBpgXex0E91ThH3G8C1FWwoiIFs0qj?usp=sharing)

## Project Overview

This project aims to **predict whether a customer will fully repay their loan** based on their application details and credit history.  
We perform **EDA**, **data preprocessing**, **model building**, and **evaluation** to understand important factors behind loan defaults and optimize predictions.

---

## Dataset

- **Source:** [Download Data](https://drive.google.com/file/d/1ZPYj7CZCfxntE8p2Lze_4QO4MyEOy6_d/view?usp=sharing)
- **Size:** ~80,000 records
- **Features:** Loan amount, installment, home ownership, income, grade, employment title, etc.

---

## Problem Statement

Given historical loan applications, predict if a customer will **fully pay** or **default**.

- **Target variable:** `loan_status` (1 = Fully Paid, 0 = Defaulted)

---

## Colab Notebook

🔗 [Click to View Full Code in Google Colab](https://colab.research.google.com/drive/1PBFBpgXex0E91ThH3G8C1FWwoiIFs0qj?usp=sharing)

---

## Project Steps

1. **Data Loading & Preprocessing**
   - Handling missing values
   - Dropping unnecessary columns like `emp_title`
   - Encoding categorical variables

2. **Exploratory Data Analysis (EDA)**
   - Loan amount vs installment correlation
   - Home ownership distribution
   - Fully paid rates by grades

3. **Model Building**
   - Logistic Regression
   - Class balancing techniques (Class Weights and SMOTE)

4. **Threshold Optimization**
   - Finding best threshold based on **F1 score**
   - Testing performance at custom thresholds

5. **Model Evaluation**
   - Accuracy
   - Precision, Recall, F1-Score
   - ROC-AUC
   - Confusion Matrix

---

## Key Results

| Metric | Default Threshold (0.4) | Best Threshold (0.13) |
|:------|:-------------------------|:----------------------|
| Accuracy | 75.01% | 80.53% |
| Recall (Defaults) | 43% | 2% |
| Precision (Defaults) | 38% | 59% |
| ROC AUC | ~0.83 | ~0.85 |

- **Primary metric to focus:** Recall (important for catching defaulters)
- **Top Influential Features:** `term`, `dti`, `int_rate`, `annual_inc`, `sub_grade`, etc.
- **Affected by Geography:** No (based on available features)

---

## Recommendations

- **Recall priority:** Since missing defaulters is riskier than false positives for banks.
- **Class imbalance:** Use Class Weighting and custom threshold for better handling.
- **Feature Engineering:** More powerful features can improve performance.

---

## How to Run

> You can open the notebook directly in **Google Colab** (no installation needed!)

- Click [here](https://colab.research.google.com/drive/1PBFBpgXex0E91ThH3G8C1FWwoiIFs0qj?usp=sharing).
- Download the dataset and upload when prompted.
- Run cells sequentially.

---

## Author

- ✨ *Built with guidance and passion for ML projects!* ✨

---
