# Predicting Mental Health Treatment-Seeking Behavior Among Tech Professionals

## Overview
This project predicts mental health treatment-seeking behavior among technology professionals using machine learning. The study identifies key factors influencing whether tech employees seek help, providing actionable insights for workplace well-being.



## Dataset
An anonymized survey dataset of 1,233 tech professionals covering:  
- **Demographics:** Age, gender, region  
- **Workplace factors:** Company size, remote work, mental health benefits  
- **Personal mental health history and attitudes**  
- **Treatment-seeking behavior** (target variable)

## Methodology
The workflow included:  
1. **Data Cleaning & Preprocessing:** Handling missing values, removing duplicates, outlier treatment, grouping gender and regions.  
2. **Exploratory Data Analysis (EDA):** Visualizations of demographics, treatment by gender, employer support, and family history.  
3. **Feature Engineering:** Created a `support_score` based on access to benefits, care options, wellness programs, and employer resources. 
4. **Model Training:** Evaluated Logistic Regression, Random Forest, SVM, and XGBoost.  
5. **Model Tuning:** The two best-performing models (Logistic Regression and XGBoost) were optimized using **GridSearchCV with 5-fold cross-validation**, selecting hyperparameters that maximized ROC-AUC.  
6. **Model Evaluation:** Metrics included Accuracy, Precision, Recall, F1-Score, ROC-AUC; Confusion matrices and ROC curves were plotted for interpretability.  
7. **Interpretability:** SHAP values were used to explain feature importance and understand which variables drive predictions.

## Results

**Performance of Tuned Models:**  

| Model               | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|--------------------|---------|----------|--------|---------|---------|
| Logistic Regression | 0.717   | 0.726    | 0.714  | 0.720   | 0.832   |
| XGBoost             | 0.725   | 0.738    | 0.714  | 0.726   | 0.827   |

XGBoost slightly outperformed Logistic Regression, and both models achieved strong ROC-AUC scores, indicating robust predictive performance.

## Key Insights from SHAP Analysis
- **Work Interference:** Higher interference with personal life increases likelihood of seeking treatment.  
- **Family History of Mental Health Issues:** Individuals with affected family members are more likely to seek help.  
- **Health Care Opportunities:** Access to employer mental health resources boosts treatment-seeking.  
- **Age:** Older employees are more likely to seek treatment.  
- **Employer Support:** Programs providing leave, anonymity, and wellness initiatives encourage help-seeking.

## Visualizations
- Age and gender distribution  
- Treatment-seeking behavior across demographics  
- Employer support and company size  
- Confusion matrices and ROC curves  
- SHAP summary plots showing feature importance  

## Tools & Technologies
- **Python 3.x**, **Pandas**, **NumPy**  
- **Matplotlib**, **Seaborn**  
- **Scikit-learn**, **XGBoost**, **SHAP**  
- **Jupyter Notebook / Google Colab**

## Nisanth Jose
