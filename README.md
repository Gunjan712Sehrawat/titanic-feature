# Titanic Feature Engineering 

This project contains code and artifacts for data cleaning and feature engineering on the Titanic dataset.

Files:
- titanic.csv           : original dataset (seaborn sample)
- cleaned_titanic.csv   : cleaned + engineered dataset (ready for ML)
- logreg_titanic.pkl    : trained Logistic Regression model (if trained)
- requirements.txt      : required Python packages

Steps performed:
- Missing value handling (age, fare, embarked)
- Title extraction (if 'name' exists)
- FamilySize and IsAlone features
- HasCabin feature
- AgeGroup categories
- One-hot encoding for categorical variables
- Feature scaling (excluding the 'survived' target)
- Quick logistic regression model training/evaluation
