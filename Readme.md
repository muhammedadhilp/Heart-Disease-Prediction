# Heart Disease Prediction Project
## Overview
This project focuses on predicting the likelihood of heart disease in patients based on a range of clinical features such as age, sex, chest pain type, blood pressure, and others. Using a logistic regression model, we aim to classify patients into two categories: those with a high chance of heart disease and those with a low chance.

## Dataset Description
The dataset contains a variety of clinical features related to cardiovascular health. Below are the features:

## Features:
Age: Age of the patient (years).
Sex: Gender of the patient (1 = male, 0 = female).
cp (Chest Pain Type):
Value 1: Typical Angina
Value 2: Atypical Angina
Value 3: Non-anginal Pain
Value 4: Asymptomatic
trtbps: Resting blood pressure in mmHg.
chol: Serum cholesterol in mg/dl fetched via BMI sensor.
fbs (Fasting Blood Sugar): Whether fasting blood sugar > 120 mg/dl (1 = true, 0 = false).
restecg: Resting electrocardiographic results:
Value 0: Normal
Value 1: ST-T wave abnormality (e.g., T wave inversions)
Value 2: Showing probable or definite left ventricular hypertrophy.
thalach: Maximum heart rate achieved.
exang: Exercise-induced angina (1 = yes, 0 = no).
oldpeak: ST depression induced by exercise relative to rest.
slp (Slope of ST segment during exercise):
Value 0: Downsloping
Value 1: Flat
Value 2: Upsloping.
ca: Number of major vessels colored by fluoroscopy (0–3).
thal: Thalassemia (a genetic blood disorder):
Value 0: No data
Value 1: Fixed defect
Value 2: Reversible defect.
target: Output class:
0 = Less chance of heart attack
1 = More chance of heart attack.
## Exploratory Data Analysis (EDA)
Summary of Statistics:
### Age:

Mean: 54.37 years
Range: 29 to 77 years.
### Sex:

Skewed towards males (68% male).
### Chest Pain Type (cp):

Majority patients fall into lower categories (1 and 2).
### Resting Blood Pressure (trtbps):

Mean: 131.62 mmHg (slightly above normal).
### Cholesterol (chol):

Mean: 246.26 mg/dl (high cholesterol levels observed).
### Fasting Blood Sugar (fbs):

Most patients have normal fasting blood sugar.
### Resting ECG (restecg):

Common abnormal findings (mean around 1).
### Maximum Heart Rate (thalach):

Mean: 149.65 bpm (healthy range).
### Exercise-Induced Angina (exang):

Most patients do not experience exercise-induced angina.
### ST Depression (oldpeak):

Mean: 1.04 (mild depression).
### Slope of the ST Segment (slp):

Flat or upsloping segments mostly seen.
### Major Vessels Colored by Fluoroscopy (ca):

Most patients show 0-1 vessels blocked.
### Thalassemia (thal):

The majority show a fixed or reversible defect.
### Output (Heart Disease Presence):

Balanced dataset with around 54% patients having heart disease.
## Data Quality Insights:
No missing values in the dataset.
One duplicated entry.
Outliers in resting blood pressure, cholesterol, maximum heart rate, ST depression, and other features were detected but retained in the model due to their significance in clinical diagnoses.
## Visualization
Count plots were created to examine the distribution of heart disease in relation to other variables like sex, chest pain type, etc.
A correlation matrix was generated to understand feature relationships, revealing some correlation between features like chest pain type and heart disease likelihood.
## Preprocessing
Standardization: The continuous features such as blood pressure, cholesterol, and heart rate were standardized using StandardScaler.
Train-Test Split: Data was split into 80% training and 20% test sets.
## Model Training
A Logistic Regression model was chosen for its simplicity and effectiveness in binary classification tasks.

## Model Performance:
Accuracy: 83.61%
Precision, Recall, F1-Score: Provided in the classification report.
Confusion Matrix: Visualized to assess model performance on the test data.
## Key Insights from Model:
Features like chest pain type, resting blood pressure, and cholesterol are significant indicators for heart disease.
The model performs well, but fine-tuning and testing other models (such as decision trees, SVMs) could provide a better result.
## Project Requirements
### Python (3.x)
### Libraries:
pandas,numpy,matplotlib,seaborn,scikit-learn,scipy
## How to Run the Code:
### Install the required dependencies:
pip install pandas numpy matplotlib seaborn scikit-learn scipy
Download the dataset and save it as heart.csv.
Run the Jupyter Notebook or Python script to explore the data, visualize relationships, and train the model.
The model will output accuracy, classification report, and confusion matrix.
## Conclusion:
This project provides a basic understanding of heart disease prediction using logistic regression. The dataset contains rich clinical information that can be further explored with more advanced models. The findings could help in understanding key cardiovascular risk factors and aid in medical decision-making.

## Future Work:
Experiment with more complex models (e.g., Random Forest, Neural Networks).
Perform hyperparameter tuning for better results.
Explore feature engineering to improve model accuracy.

