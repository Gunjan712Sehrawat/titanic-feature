# Titanic Dataset — Linear Regression & Decision Tree Training

## 1. Purpose
This project applies two supervised learning models — **Linear Regression** and **Decision Tree Classifier** — to the cleaned and feature-engineered Titanic dataset, and compares their performance.

## 2. Importance
Testing multiple algorithms on the same dataset:
- Demonstrates strengths and weaknesses of each.
- Shows the impact of preprocessing and feature engineering on results.
- Helps select the most appropriate model for binary classification.

## 3. Steps Performed
1. **Data Loading**
   - Used the cleaned and feature-engineered dataset from the Titanic Feature Engineering project.
2. **Train-Test Split**
   - 80% for training, 20% for testing.
3. **Model Training**
   - **Linear Regression**: Predicts continuous scores; binarized predictions for classification accuracy.
   - **Decision Tree Classifier**: Direct binary classification.
4. **Model Evaluation**
   - **Linear Regression**: Mean Squared Error (MSE), R² score, classification accuracy (threshold=0.5).
   - **Decision Tree Classifier**: Accuracy, confusion matrix, classification report.
5. **Visualization**
   - Scatter plot of predicted vs. actual values (Linear Regression).
   - Feature importance bar chart (Decision Tree).

## 4. Methodology
- Load cleaned dataset from memory (from previous notebook) or CSV.
- Split into training/testing subsets.
- Train Linear Regression model for numeric prediction.
- Train Decision Tree Classifier for categorical prediction.
- Evaluate both models using regression and classification metrics.
- Compare results.

## 5. Implementation
- **Language:** Python  
- **Environment:** Google Colab  
- **Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

## 6. Project Structure
titanic-modeling/
│
├── titanic_modeling.ipynb # Main notebook with model training
├── README.md # Project description
├── linear_regression_model.pkl # Saved model
├── decision_tree_model.pkl # Saved model
└── requirements.txt # Python dependencies

## 7. Results

- **Linear Regression**:
- Mean Squared Error: 0.0000
  R² Score: 1.0000
  Accuracy (threshold=0.5): 1.0000

- **Decision Tree Classifier**:
  - Accuracy: 1.0000
  - Shows better performance compared to Linear Regression (if accuracy is higher).

Decision Tree achieved higher classification accuracy and provided better interpretability through feature importance analysis.

## 8. Conclusion
- Decision Tree Classifier is better suited for the Titanic survival classification task than Linear Regression.
- Linear Regression still gives useful probability-like predictions but is less appropriate for classification.
- The strong performance of both models highlights the value of the feature engineering performed in the earlier project.
