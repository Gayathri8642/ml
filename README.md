# Water Quality Prediction Using Machine Learning

## Project Overview

This project focuses on predicting whether water is safe for drinking using Machine Learning algorithms. The system analyzes different physical and chemical properties of water and classifies the water as potable (safe) or non-potable (unsafe).

The project uses data preprocessing, feature scaling, feature selection, and multiple machine learning models to improve prediction performance.

---

# Objective

The main objective of this project is to:

* Analyze water quality parameters
* Handle missing values in the dataset
* Preprocess and normalize data
* Train machine learning models
* Predict water potability
* Compare model performance using evaluation metrics

This system helps automate water quality analysis and supports intelligent decision-making for safe drinking water.

---

# Technologies Used

## Programming Language

* Python

## Libraries Used

* pandas
* numpy
* matplotlib
* scikit-learn
* xgboost

---

# Dataset Description

The dataset contains **3276 water samples** with **10 attributes**.

## Input Features

| Feature         | Description                                     |
| --------------- | ----------------------------------------------- |
| ph              | Measures acidity or alkalinity of water         |
| Hardness        | Amount of dissolved calcium and magnesium       |
| Solids          | Total dissolved solids in water                 |
| Chloramines     | Chemical disinfectants present in water         |
| Sulfate         | Sulfate concentration                           |
| Conductivity    | Electrical conductivity of water                |
| Organic_carbon  | Organic carbon amount                           |
| Trihalomethanes | Harmful compounds formed during water treatment |
| Turbidity       | Cloudiness of water                             |

## Target Variable

| Column     | Meaning                           |
| ---------- | --------------------------------- |
| Potability | 1 = Safe for drinking, 0 = Unsafe |

---

# Project Workflow

Dataset Collection
↓
Data Cleaning
↓
Missing Value Handling
↓
Feature Scaling
↓
Feature Selection
↓
Train-Test Split
↓
Model Training
↓
Prediction
↓
Performance Evaluation

---

# Data Preprocessing

## 1. Handling Missing Values

The dataset contained missing values in the following columns:

* ph
* Sulfate
* Trihalomethanes

Missing values were replaced using the mean value of each column using Mean Imputation.

### Advantages of Mean Imputation

* Maintains dataset size
* Avoids loss of important records
* Keeps data distribution balanced

---

## 2. Feature Scaling

MinMaxScaler was used to normalize all feature values between 0 and 1.

### Why Scaling is Important?

Different features have different ranges. Scaling helps:

* Improve model performance
* Prevent domination of large values
* Increase training efficiency
* Improve convergence speed

---

# Feature Selection

Recursive Feature Elimination (RFE) was used with Random Forest Classifier to identify the most important features.

## Important Features Selected

* ph
* Hardness
* Solids
* Chloramines

These features contributed more significantly toward water quality prediction.

---

# Machine Learning Models Used

## 1. Random Forest Classifier

Random Forest is an ensemble learning algorithm that creates multiple decision trees and combines their outputs.

### Advantages

* High accuracy
* Reduces overfitting
* Handles nonlinear data effectively
* Good classification performance

### Results

* Accuracy: 68.59%
* Precision: 65.08%
* Recall: 33.60%

---

## 2. XGBoost Classifier

XGBoost (Extreme Gradient Boosting) is an advanced boosting algorithm used for efficient prediction.

### Advantages

* Fast and efficient
* Handles complex patterns
* Improves prediction accuracy
* Widely used in real-world applications

### Results

* Accuracy: 65.54%
* Precision: 54.78%
* Recall: 42.21%

---

## 3. Support Vector Machine (SVM)

GridSearchCV was used with SVM for hyperparameter tuning.

### Parameters Tested

* Kernel: Linear, Sigmoid
* C Values: 1, 200

### Best Parameters

```python
{'C': 1, 'kernel': 'linear'}
```

### Best Accuracy

* 60.53%

---

# Evaluation Metrics

## Accuracy

Measures the overall correctness of the model.

## Precision

Measures how many predicted positive values are actually correct.

## Recall

Measures how many actual positive values are correctly identified.

## Confusion Matrix

Used to evaluate prediction performance by comparing actual and predicted values.

---

# Model Comparison

| Model | Accuracy | Precision | Recall |
|---|---|---|
| Random Forest | 68.59% | 65.08% | 33.60% |
| XGBoost | 65.54% | 54.78% | 42.21% |
| SVM | 60.53% | - | - |

---

# Conclusion

This project successfully predicts water potability using Machine Learning techniques.

The system performs:

* Data preprocessing
* Missing value handling
* Feature scaling
* Feature selection
* Model training and evaluation

Among all the models tested, the Random Forest Classifier achieved the highest accuracy.

The project demonstrates how machine learning can help automate water quality assessment and support safer water management systems.

---

# Future Enhancements

* Improve accuracy using deep learning models
* Deploy the model as a web application
* Use larger real-time datasets
* Add graphical visualizations and dashboards
* Integrate IoT sensors for live water monitoring

---

# Author

Developed as a Machine Learning project for Water Quality Prediction using Python and Machine Learning algorithms.
