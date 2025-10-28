# Autism Prediction Using Supervised Learning

## Overview

This project aims to predict whether a person is likely to have Autism Spectrum Disorder (ASD) using various supervised machine learning algorithms. The dataset is taken from the [Kaggle Autism Prediction Challenge](https://www.kaggle.com/competitions/autism-prediction/).

The project includes exploratory data analysis (EDA), data preprocessing, feature visualization, model training, and performance comparison to identify the best-performing classification model.

---

## Dataset Description

The dataset contains **800 records** with multiple features related to demographics, behavioral scores, and screening results.

| Feature                | Description                                       |
| ---------------------- | ------------------------------------------------- |
| `A1_Score`–`A10_Score` | Autism screening questionnaire scores             |
| `age`                  | Participant's age                                 |
| `gender`               | Gender of participant                             |
| `ethnicity`            | Ethnic background                                 |
| `jaundice`             | Whether participant had jaundice at birth         |
| `austim`               | Whether there’s a family history of autism        |
| `contry_of_res`        | Country of residence                              |
| `used_app_before`      | Whether participant used the screening app before |
| `result`               | Screening result score                            |
| `Class/ASD`            | Target variable (1 = ASD, 0 = Not ASD)            |

---

## Data Preprocessing

* Checked for **missing values** (none found)
* Converted categorical variables using **Label Encoding** and **One-Hot Encoding**
* Scaled numerical features using **StandardScaler**
* Split dataset into **training (80%)** and **testing (20%)** sets

---

## Exploratory Data Analysis (EDA)

Key insights from data visualization:

* Most participants were from a few dominant countries.
* The dataset had slightly more **male** participants than females.
* Family history of autism and higher screening scores correlated with ASD diagnosis.
* Age distribution was mostly concentrated between **20–40 years**.

---

## Model Training and Evaluation

Five supervised learning models were trained and evaluated using Accuracy, F1-Score, and ROC AUC metrics.

### **Final Model Comparison (Sorted by ROC AUC)**

| Model               | Accuracy | F1-Score |   ROC AUC  |
| :------------------ | :------: | :------: | :--------: |
| **Random Forest**   | **0.85** |   0.613  | **0.9145** |
| SVM                 |   0.825  |   0.682  |   0.8952   |
| XGBoost             |   0.838  |   0.606  |   0.8819   |
| Logistic Regression |   0.863  |   0.694  |   0.8808   |
| K-Nearest Neighbors |   0.825  |   0.563  |   0.8495   |

---

## Best Model

**Random Forest Classifier** demonstrated the highest **ROC AUC (0.91)**, showing strong discriminative power between ASD and non-ASD cases.
It also provided a good balance of accuracy and interpretability compared to other models.

---

## Tools & Libraries Used

* **Python 3.11+**
* **Pandas**, **NumPy** — data manipulation
* **Matplotlib**, **Seaborn** — visualization
* **Scikit-learn** — model building and evaluation
* **XGBoost** — gradient boosting model

---

## Future Improvements

* Perform hyperparameter tuning for better accuracy
* Apply feature selection to reduce dimensionality
* Explore ensemble methods combining Random Forest and XGBoost
* Consider deep learning approaches for higher generalization

---

## Author

**Sushma Suresh**
*MS-AI Program — Supervised Learning Final Project*

