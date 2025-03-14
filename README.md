# Predicting-PCOS-Using-Lifestyle-Factors
PCOS Lifestyle Impact Research - Kaggle Competition



# Exploring Predictive Health Factors - PCOS Lifestyle Impact

## Competition Overview

Polycystic ovary syndrome (PCOS) is a common endocrine disorder affecting reproductive health and quality of life. Research indicates that lifestyle factors such as diet, exercise, and stress management significantly influence PCOS symptoms. However, gaps remain in understanding the individual and combined effects of these lifestyle choices.    

This competition aimed to analyze lifestyle impacts on PCOS using data-driven methods to support clinical intervention and health management. The objective was to build predictive models that classify PCOS based on various health and lifestyle features.   

## Evaluation Metric

Submissions were evaluated using the Area Under the ROC Curve (AUC-ROC), which measures the model’s ability to distinguish between positive and negative PCOS cases.    

## Rank & Score

**Rank: 14 / 139**    

**Public Score: 0.955 (AUC-ROC)**    

**Private Score: 0.804 (AUC-ROC)**    


While AdaBoost initially performed well on the public leaderboard, its private score revealed signs of overfitting. This highlights the importance of robust validation strategies. Post-competition analysis suggests that CatBoost, with better hyperparameter tuning and feature engineering, could have been a more stable model choice.    

## Dataset Overview

Train Set: 210 rows, 14 columns    

Test Set: 145 rows, 13 columns    


## Columns:

Features: Age, Weight (kg), Hormonal Imbalance, Hirsutism, Conception Difficulty, Insulin Resistance, Exercise Frequency, Exercise Type, Exercise Duration, Sleep Hours, Exercise Benefit.

Target Variable: PCOS (Binary: 1 = PCOS, 0 = No PCOS).    


*Some categorical variables were misaligned or incorrectly formatted, requiring preprocessing before model training.*   

## Data Preprocessing & Feature Engineering    

1. Data Cleaning: Fixed column misalignment, corrected wrong values.    


2. Outlier Handling: Used Interquartile Range (IQR) method.   


3. Missing Value Treatment: Applied mode, median, and manual imputation separately for train and test sets.    


4. Feature Engineering:   

PCOS Severity Score   

Lifestyle Score    

Reproductive Risk Score    

Sleep Deficiency Indicator    



5. Encoding: Manually mapped categorical variables.   


6. Balancing: Applied SMOTE to handle class imbalance.    



## Modeling Approach

Tested multiple machine learning models:    

**Random Forest (Private AUC-ROC: 0.806, Public AUC-ROC: 0.899)**    

**XGBoost**    

**LightGBM**    

**AdaBoost (Selected model: Public AUC-ROC 0.955, Private AUC-ROC 0.804)**    

**H2O GBM**   

**Neural Networks**    

**Extra Trees Classifier**     

**CatBoost (Private AUC-ROC: 0.812, Public AUC-ROC: 0.871)**    


AdaBoost initially showed the highest public score, but post-competition analysis suggests that CatBoost, with further tuning, could have been a better choice.

## Key Learnings

Overfitting Awareness: The difference between public and private scores reinforced the importance of robust cross-validation.

Feature Engineering Impact: Adding domain-specific features significantly improved model performance.

Model Selection Strategy: More focus on generalization could improve leaderboard stability.
