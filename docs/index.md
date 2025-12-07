# Gastrointestinal Illness Prediction from Beach Water Quality  
### Project Documentation for GitHub Pages

This website accompanies the machine learning project analyzing gastrointestinal (GI) illness severity among beachgoers exposed to contaminated ocean water at Santa Monica Bay. The project evaluates how microbial water indicators, swimmer demographics, and exposure conditions relate to illness severity.

---

## Project Background

The Santa Monica Bay Epidemiological Study collected environmental and health data from over 11,000 swimmers across three beaches. After cleaning and preprocessing, the analytical dataset consisted of **8,944 participants**.

The data included:
- Microbial water quality indicators (total coliform, fecal coliform, *E. coli*, enterococcus)  
- Demographic variables (age, sex, race)  
- Exposure metrics (distance from storm drains)  
- Illness symptoms and GI severity score (QG)

Because this dataset contains sensitive information, it is not included in this repository. However, all modeling code is documented in the included Jupyter Notebook.

---

## Modeling Overview

Four models were developed:

### Regression
- Multiple Linear Regression  
- Random Forest Regressor  

### Classification
- Logistic Regression with L1 penalty  
- XGBoost Classifier  

Preprocessing steps included:
- Log transformations of bacterial indicators  
- Log transformation of QG severity  
- One-hot encoding  
- Outlier treatment  
- SMOTE balancing  
- LassoCV feature selection  
- Random Forest importance ranking  

---

## Summary of Findings

### Regression Results
- Linear Regression R² = **0.526**  
- Random Forest R² = **0.522**  
Both performed nearly identically, suggesting the transformed data had predominantly linear relationships.

### Classification Results
- Logistic Regression: **62% accuracy**, F1 = 0.556  
- XGBoost: **58.8% accuracy**, F1 = 0.579  
XGBoost produced more balanced predictions and better identified high-severity cases.

### Key Predictors
- Total coliform was the strongest microbial predictor  
- Symptom variables strongly predicted continuous severity  
- Age, race, and distance from storm drains influenced predictions  

---

## Repository Structure

- Full modeling code: `analysis.ipynb`  
- Project README: `README.md`  
- This documentation page: `docs/index.md`



