🩺 Heart Disease Prediction Analysis
🎯 Task Objective
The goal of this project is to develop a machine learning model capable of predicting whether a patient is at risk of heart disease based on several clinical health markers. This is a Binary Classification task where the model learns to distinguish between "Healthy" and "Heart Disease" states using the UCI Heart Disease dataset.

📊 Dataset Overview
The project utilizes the Heart Disease UCI Dataset (sourced from Kaggle). It contains 303 cases with 14 key health features.

Key Features Included:
Age & Sex: Basic demographic data.

Chest Pain (cp): Type of chest pain experienced (4 levels).

Resting BP (trestbps): Blood pressure at rest.

Cholesterol (chol): Serum cholesterol in mg/dl.

Max Heart Rate (thalach): Maximum heart rate achieved during exercise.

Oldpeak: ST depression induced by exercise relative to rest.

🛠️ Technical Workflow
1. Data Cleaning & Preprocessing
Handling Missing Values: Imputed missing values using the median for numerical data and the mode for categorical data.

One-Hot Encoding: Converted categorical variables (like cp and thal) into binary dummy variables to make them readable for the model.

Feature Scaling: Applied StandardScaler to ensure that features like Cholesterol (200+) do not numerically overwhelm features like Sex (0 or 1).

2. Exploratory Data Analysis (EDA)
Analyzed correlations between health markers.

Identified that Chest Pain type and Maximum Heart Rate are among the strongest indicators of heart health in this dataset.

3. Machine Learning Model
Algorithm: Logistic Regression (chosen for its high interpretability in medical diagnostics).

Training: 80/20 train-test split with a fixed random_state for reproducibility.

🚀 Evaluation Metrics
To ensure the model is reliable for clinical use, multiple metrics were used:

Accuracy: Overall percentage of correct predictions.

Confusion Matrix: Used to monitor False Negatives (the most dangerous error in medicine).

ROC-AUC Curve: Measured the model's ability to distinguish between classes. A higher Area Under the Curve (AUC) indicates a more robust diagnostic tool.

📈 Key Findings
Primary Risk Factors: Based on feature importance, high ST depression (oldpeak) and specific Chest Pain types were the most significant predictors of disease.

Model Performance: The model achieved an accuracy of approximately [Insert your accuracy, e.g., 85%], with a strong AUC score.
