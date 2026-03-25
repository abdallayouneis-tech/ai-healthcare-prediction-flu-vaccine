# ai-healthcare-prediction-flu-vaccine
Machine learning pipeline for predicting H1N1 and seasonal flu vaccination using ensemble models and feature engineering


This project develops a machine learning pipeline to predict H1N1 and seasonal flu vaccination behavior using large-scale healthcare survey data.

The goal is to model vaccination uptake using demographic, behavioral, and perception-based features, while addressing challenges such as class imbalance, missing data, and heterogeneous feature types.
________________________________________
Key Highlights
•	Built an end-to-end ML pipeline for healthcare prediction
•	Achieved AUC ~0.86 using ensemble modeling
•	Applied advanced feature engineering and selection techniques
•	Implemented stacked ensemble models (LightGBM, XGBoost, Random Forest)
•	Performed hyperparameter tuning using Optuna
•	Extracted interpretable insights on vaccination behavior
________________________________________
Problem Statement

Predict whether an individual receives:
•	H1N1 flu vaccine
•	Seasonal flu vaccine

Based on:
•	Demographics
•	Behavioral patterns
•	Risk perception
________________________________________
Methodology

1. Data Preprocessing
•	Missing value handling:
o	Mean imputation (numerical)
o	Mode / “missing” (categorical)
•	Feature scaling:
o	StandardScaler
•	Encoding:
o	One-Hot Encoding (OHE)
________________________________________
2. Feature Engineering
•	Created derived features from behavioral and perception variables
•	Tested clustering-based feature augmentation (not retained due to performance drop)
________________________________________
3. Feature Selection
•	Wrapper method using CatBoost
•	Correlation filtering (threshold > 0.8)
•	Reduced dimensionality while improving model performance
________________________________________
4. Handling Class Imbalance
•	Applied:
o	Class weighting
o	scale_pos_weight tuning
________________________________________
5. Modeling Approach

Tested multiple models:
•	Logistic Regression
•	KNN
•	Naïve Bayes
•	Decision Trees
•	Random Forest
•	XGBoost
•	LightGBM
________________________________________
Final Model: Stacked Ensemble

Combined:
•	LightGBM
•	XGBoost
•	Random Forest

Result:
Best AUC: ~0.8638
________________________________________
6. Hyperparameter Optimization
•	Used Optuna for efficient search
•	Improved model performance by ~1–2% AUC
________________________________________
Key Insights

Top predictive features included:
•	Age group
•	Perceived risk of infection
•	Beliefs about vaccine effectiveness

Behavioral perception plays a major role in vaccination decisions.
