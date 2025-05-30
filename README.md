# Diabetes Risk Prediction

## Overview
In this project, I used a CDC‐sourced dataset of over 250,000 records to predict diabetes status (diagnosed vs. not) via five different machine‐learning models: Logistic Regression, Support Vector Machine, Decision Tree, Random Forest, and AdaBoost. Uniquely, I compared each model’s AUC performance, extracted its top predictor, and then conducted an ensemble‐level analysis to identify the overall best approach. An extra‐credit exploration examined feature interactions—particularly how BMI and lifestyle factors jointly influence diabetes risk.

## Features
- **Data Preparation:** Loaded `diabetes.csv`, split into train/test sets, and handled any missing values.  
- **Model Training & Evaluation:**  
  - **Logistic Regression** for baseline binary classification  
  - **Support Vector Machine (SVM)** with linear kernel  
  - **Single Decision Tree** classifier  
  - **Random Forest** ensemble of 100 trees  
  - **AdaBoost** boosting of decision‐tree stumps  
- **Performance Metrics:** Computed ROC curves and AUC for each model on the test set.  
- **Feature Importance:** Identified each model’s strongest predictor via coefficients or importance scores.  
- **Comparative Analysis:** Ranked all five models by AUC to determine the most effective approach.  
- **Extra Insights:** Explored BMI × lifestyle interactions for deeper epidemiological insight.

## Tech & Tools
- **Language:** Python 3  
- **Data Handling:** pandas, NumPy  
- **Modeling:** scikit-learn (LogisticRegression, SVC, DecisionTreeClassifier, RandomForestClassifier, AdaBoostClassifier)  
- **Evaluation & Visualization:** Matplotlib, Seaborn  
- **Environment:** Jupyter Notebook 
- **Version Control:** Git & GitHub  

## Results & Key Takeaways
- **Logistic Regression:**  
  - **Best Predictor:** High blood pressure (`HighBP`) (coefficient ≈ 0.764)  
  - **AUC:** 0.8252  
- **Support Vector Machine (SVM):**  
  - **Best Predictor:** Body Mass Index (`BMI`)  
  - **AUC:** ~0.83  
- **Decision Tree:**  
  - **Best Predictor:** `BMI` (highest feature importance)  
  - **AUC:** ~0.78  
- **Random Forest:**  
  - **Best Predictor:** `BMI`  
  - **AUC:** ~0.88  
- **AdaBoost:**  
  - **Best Predictor:** `BMI`  
  - **AUC:** ~0.89  
- **Top Model:** AdaBoost achieved the highest AUC, demonstrating the power of boosting on this dataset.  
- **Lifestyle Interaction:** Preliminary analysis suggests that high BMI combined with low physical activity further elevates diabetes risk—an insight for targeted prevention strategies.

## Skills Gained
Binary Classification, Model Evaluation, Feature Importance Analysis, and Data Exploration.
 

## Quick Start

1. **Clone the repo**  
   ```bash
   git clone https://github.com/yourusername/diabetes-risk-prediction.git
   cd diabetes-risk-prediction
