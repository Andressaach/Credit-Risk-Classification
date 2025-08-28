# Credit Risk Classification Project

## 📌 Overview  
This project aims to predict the credit risk of individuals using the **German Credit Dataset**, helping financial institutions reduce defaults and improve loan decision-making processes.  

---

## 🎯 Objectives  
- Perform **Exploratory Data Analysis (EDA)** to understand data distributions and relationships.  
- Apply **data preprocessing** techniques, including handling outliers, scaling, and categorical encoding.  
- Build, tune, and compare **Machine Learning models** for binary credit risk classification.  
- Evaluate models using multiple performance metrics: **accuracy, precision, recall, F1-score, and ROC AUC**.
  
---

## 📊 Dataset  
- **Source**: German Credit Dataset (UCI Machine Learning Repository)  
- **Features**: 10 attributes, such as age, credit history, loan duration, and purpose.  
- **Target Variable**: `CreditRisk` (binary classification):  
  - `True` → good credit risk  
  - `False` → bad credit risk  

---

## 🛠️ Tools & Technologies  
- **Language**: Python  
- **Libraries**: pandas, numpy, scikit-learn, matplotlib, seaborn  
- **Environment**: Jupyter Notebook  

---

## 🔄 Workflow  
1. **Data Preprocessing**  
   - Handle missing values  
   - Encode categorical variables  
   - Normalize numerical features  

2. **Exploratory Data Analysis (EDA)**  
   - Analyze distributions and outliers  
   - Study correlations between features  
   - Identify relevant patterns

3. **Modeling**  
   - Algorithms used:  
     - Logistic Regression  
     - Decision Tree  
     - Random Forest  
   - **Hyperparameter tuning** with `GridSearchCV`  

4. **Evaluation**  
   - Accuracy, Precision, Recall, F1-score  
   - ROC AUC  
   - Confusion matrix analysis  

---

## 📈 Results  

| Model                  | Accuracy | Precision | Recall | F1-score | ROC AUC |
|-------------------------|----------|-----------|--------|----------|---------|
| **Logistic Regression** | 0.63     | 0.64      | 0.63   | 0.63     | 0.59    |
| **Decision Tree**       | 0.64     | 0.64      | 0.64   | 0.64     | 0.58    |
| **Random Forest**       | 0.66     | 0.65      | 0.66   | 0.66     | 0.61    |

➡️ **Random Forest** achieved the best overall performance with **66% accuracy** and **ROC AUC of 0.61**, outperforming Logistic Regression and Decision Tree.  

---

## 🚀 How to Run the Project  
1. Clone the repository:  
   ```bash
   git clone https://github.com/Andressaach/Credit-Risk-Classification.git

2. Navigate to the project folder:  
   ```bash
   cd Credit-Risk-Classification
   
3. Open Jupyter Notebook and run the notebooks in order:

- 01_EDA.ipynb
- 02_preprocessing.ipynb
- 03_modeling.ipynb

