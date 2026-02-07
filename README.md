
Overview:
Predict whether a student will Pass or Fail using academic, personal,
and social information with machine learning models.
This helps teachers and institutions identify students who need
additional academic support and take early action.


Dataset:
File: student_data.csv
Source: UCI Machine Learning Repository

Columns include:
- studytime : Weekly study time
- failures  : Number of past class failures
- absences  : Number of school absences
- parental education : Father’s and mother’s education
- school support : School support availability
- family support : Family support availability
- final grade : Used to create target variable


Feature Engineering:
- Create target variable:
  Pass = 1  (final grade ≥ 10)
  Fail = 0  (final grade < 10)
- Remove grade columns (G1, G2, G3) to avoid data leakage
- Convert categorical columns to numeric using label encoding
- Separate features (X) and target (y)
- Split data into training and testing sets


Preprocessing:
- Remove irrelevant and leakage columns
- Encode categorical values into numbers
- Handle class imbalance using stratified train-test split
- Prepare clean numeric data for machine learning models


Models:
The following machine learning models are trained and compared:

1. Logistic Regression
   - Used as a baseline classification model

2. Random Forest Classifier
   - n_estimators = 300
   - max_depth = 12
   - class_weight = balanced
   - random_state = 42

3. Gradient Boosting Classifier
   - n_estimators = 300
   - learning_rate = 0.05
   - random_state = 42


Evaluation Metrics:
Since this is a classification problem, the following metrics are used:
- Accuracy       : Measures how many students are correctly classified
- F1 Score       : Balances precision and recall
- Confusion Matrix : Shows correct and incorrect predictions


How to Run:
- Install required libraries:
  pandas, numpy, scikit-learn, matplotlib, seaborn
- Place student-mat.csv in the project folder
- Run the notebook or Python script
