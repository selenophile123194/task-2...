# task-2...
Build an end-to-end machine learning pipeline using the scikit-learn Pipeline API to predict customer churn
Telco Customer Churn Prediction Pipeline
This notebook demonstrates an end-to-end machine learning pipeline built using scikit-learn to predict customer churn for a telecommunications company.

Dataset
The dataset used in this project is the Telco Customer Churn dataset, available from: https://raw.githubusercontent.com/IBM/watson-machine-learning-samples/master/cloud-object-storage/data/telco-customer-churn/telco.csv

Pipeline Overview
The pipeline includes the following steps:

Data Loading: Load the dataset into a pandas DataFrame.
Data Exploration and Preparation: Perform basic data exploration, handle missing values, and identify categorical and numerical features. The 'TotalCharges' column is handled as part of the one-hot encoding due to its mixed data type.
Preprocessing: Create a ColumnTransformer to apply StandardScaler to numerical features and OneHotEncoder to categorical features.
Model Definition: Define Pipeline objects for two different classifiers:
Logistic Regression
Random Forest
Hyperparameter Tuning: Use GridSearchCV to find the best hyperparameters for each model based on the F1-score.
Model Evaluation: Evaluate the performance of the best models on a held-out test set using metrics such as accuracy, precision, recall, and F1-score.
Model Export: Export the best performing pipeline using joblib for future use.
Code Structure
The notebook is structured into several sections, each addressing a specific step in the machine learning pipeline.

Load the dataset: Loads the data from the specified URL.
Initial Data Exploration and Preparation: Includes basic data checks and column identification.
Define Preprocessing Steps: Sets up the ColumnTransformer.
Create Machine Learning Pipelines: Defines the Pipeline objects for Logistic Regression and Random Forest.
Define Hyperparameter Grids: Specifies the parameter search space for GridSearchCV.
Evaluate Models: Trains and evaluates the models using GridSearchCV and reports the results.
Export the Best Pipeline: Saves the best performing pipeline to a file.
Load and Test Saved Pipeline: Demonstrates how to load the saved pipeline and make predictions.
Requirements
The following libraries are required to run this notebook:

pandas
numpy
scikit-learn
joblib
These can be installed using pip:

