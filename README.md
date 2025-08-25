# Credit Risk Classification Project

## Overview
Accurately assessing credit risk is crucial for financial institutions to minimize default rates and make informed lending decisions. This project aims to predict the credit risk of individuals using the **German Credit Dataset**. 

---

## Objectives
- Analyze and understand the dataset.
- Preprocess data to handle missing values, outliers, and categorical variables.
- Build and evaluate Machine Learning models to classify credit risk.
- Identify key features impacting credit risk decisions.

---

## Dataset
- Source: [German Credit Dataset](https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+data))
- Features: 20 attributes including age, credit history, employment status, and loan purpose.
- Target: `CreditRisk` – binary classification (`Good` / `Bad` credit risk).

---

## Technologies & Tools
- **Programming Languages:** Python
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn
- **Environment:** Jupyter Notebook

---

## Project Workflow
1. **Data Preprocessing**
   - Handling missing values and duplicates
   - Encoding categorical variables
   - Feature scaling

2. **Exploratory Data Analysis (EDA)**
   - Understanding variable distributions
   - Correlation analysis
   - Visualizing patterns and relationships

3. **Model Building**
   - Logistic Regression
   - Decision Tree
   - Random Forest
   - Hyperparameter tuning using GridSearchCV

4. **Model Evaluation**
   - Metrics: Accuracy, Precision, Recall, F1-score
   - Confusion matrix and feature importance analysis

5. **Insights & Recommendations**
   - Key factors affecting credit risk
   - Strategies to minimize default risk

---

## Results
| Model              | Accuracy | Precision | Recall | F1-score |
|-------------------|---------|----------|-------|---------|
| Logistic Regression | 0.75    | 0.72     | 0.68  | 0.70    |
| Decision Tree       | 0.72    | 0.70     | 0.65  | 0.67    |
| Random Forest       | 0.80    | 0.78     | 0.74  | 0.76    |

> Random Forest achieved the best performance, highlighting features such as **Credit History**, **Purpose of Loan**, and **Duration** as critical for predicting credit risk.

---

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/Andressaach/Risco-de-Credito.git
