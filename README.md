# Titanic Dataset — Feature Engineering

## 1. Purpose
The purpose of this project is to clean and enhance the Titanic dataset using feature engineering techniques.  
The engineered dataset is designed to improve the performance of machine learning models in predicting passenger survival.

## 2. Importance
Real-world datasets are often messy and incomplete.  
By applying data cleaning and feature engineering:
- Models can better identify important patterns.
- Missing and noisy data are handled systematically.
- Relationships in the data (e.g., family size, social status) become explicit features.

## 3. Steps Performed
1. **Missing Value Handling**
   - Filled missing `Age` with median value.
   - Filled missing `Fare` with median value.
   - Filled missing `Embarked` with mode.
2. **Feature Extraction**
   - Extracted passenger **Title** from `Name` (e.g., Mr, Mrs, Miss).
   - Created **FamilySize** = `SibSp` + `Parch` + 1.
   - Created **IsAlone** (1 if passenger was alone, else 0).
   - Created **HasCabin** indicator (1 if cabin info exists, else 0).
   - Created **AgeGroup** categorical bins.
3. **Encoding & Scaling**
   - Applied one-hot encoding to categorical features.
   - Scaled numeric features (excluding target variable).
4. **Quick Model Testing**
   - Trained a Logistic Regression model on the cleaned dataset to confirm improved data quality.

## 4. Methodology
- Load Titanic dataset (CSV or Seaborn built-in).
- Apply cleaning rules for missing values.
- Create additional features to improve predictive power.
- Encode categorical data into numeric format.
- Scale features to standardize ranges.
- Train and evaluate a simple model to validate improvements.

## 5. Implementation
- **Language:** Python  
- **Environment:** Google Colab  
- **Libraries:** `pandas`, `numpy`, `seaborn`, `scikit-learn`

## 6. Project Structure
titanic-feature/
│
├── data/ # Optional: cleaned dataset CSV
├── titanic_feature.ipynb # Main notebook
├── README.md # Project description
└── requirements.txt # Python dependencies

## 7. Results
- Missing values successfully handled.
- New features improved interpretability.
- Logistic Regression accuracy increased compared to using the raw dataset.

## Evaluation

📊 Logistic Regression Accuracy: 0.6942675159235668
              precision    recall  f1-score   support

           0       0.70      0.83      0.76        92
           1       0.67      0.51      0.58        65

    accuracy                           0.69       157
   macro avg       0.69      0.67      0.67       157
weighted avg       0.69      0.69      0.69       157

## 8. Conclusion
Feature engineering significantly enhances dataset quality and improves the model’s ability to learn patterns.  
The resulting dataset can be directly used for further supervised learning models, such as Decision Trees or 
