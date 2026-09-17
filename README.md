# Employee Attrition Prediction: Data Science Capstone Project

## Overview
Employee attrition is a critical challenge for modern organizations, disrupting team performance and driving up recruitment costs. This project implements an end-to-end predictive machine learning solution using the IBM HR Analytics dataset. By analyzing employee behavior and workplace dynamics, the project identifies early warning signs of turnover to help organizations transition from reactive exit interviews to proactive retention strategies[cite: 1, 2].

---

## Business Objectives
* Identify key drivers and workplace factors associated with employee attrition[cite: 1].
* Conduct exploratory data analysis (EDA) to evaluate employee demographics, compensation, and satisfaction dynamics[cite: 1].
* Build, evaluate, and compare multiple machine learning algorithms to predict attrition[cite: 1].
* Translate technical predictive metrics into actionable retention and workforce planning strategies[cite: 1, 2].

---

## Dataset Summary
* **Total Records:** 1,470 employee entries[cite: 1].
* **Feature Count:** 35 original features spanning Demographics, Job Characteristics, Compensation, Performance, Satisfaction, Career History, and Workplace Factors[cite: 1].
* **Target Variable:** `Attrition` (`Yes` / `No`)[cite: 1].
* **Class Imbalance:** 1,233 "No" records vs. 237 "Yes" records[cite: 1].

---

## Key Exploratory Insights
* **Overtime Impact:** Employees working overtime demonstrated significantly higher attrition rates compared to those without overtime demands[cite: 1].
* **Career Progression:** Lack of advancement opportunities and stagnant tenure strongly influenced resignation decisions[cite: 1, 2].
* **Workplace Satisfaction:** Variables including *Job Satisfaction*, *Environment Satisfaction*, and *Work-Life Balance* exhibited strong relationships with turnover rates.
* **Multi-Factor Influence:** Employee attrition is driven by a complex combination of workload, progression, and satisfaction factors rather than a single metric[cite: 1].

---

## Modeling & Evaluation
To prevent data leakage, training and test datasets were strictly separated prior to preprocessing. Several algorithms were evaluated:

* **Support Vector Machine (SVM):** Designated as the preferred production model[cite: 2]. While models like Gradient Boosting achieved high raw accuracy, SVM delivered the best overall balance between Precision, Recall, F1-Score, and ROC-AUC for identifying high-risk employees[cite: 2].
* **Gradient Boosting & Random Forest:** Evaluated for benchmark baseline and feature ranking comparisons[cite: 2].

### Key Performance Drivers
Feature importance analysis confirmed the top predictors of attrition:
1. **Overtime status**[cite: 2]
2. **Career progression metrics**[cite: 2]
3. **Workplace satisfaction ratings**[cite: 2]
4. **Work-life balance indicators**[cite: 2]

---

## Repository Structure
```text
employee-attrition-prediction/
│
├── data/
│   ├── raw/                  # IBM HR Analytics dataset (1,470 records)
│   └── processed/            # Preprocessed datasets
├── notebooks/
│   ├── 01_EDA.ipynb          # Statistical analysis & visualizations
│   └── 02_Modeling.ipynb     # Model training, hyperparameter tuning, & evaluation
├── src/                      # Modular scripts for data pipeline & transformations
├── reports/
│   └── figures/              # Exported visualizations and confusion matrices
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt          # Python dependencies
