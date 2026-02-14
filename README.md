#### 🏠 End-to-End Machine Learning Pipeline Using Scikit-learn Pipeline API

#### 📌 Objective of the Task

The objective of this task is to build a complete end-to-end machine learning pipeline using Scikit-learn’s Pipeline and ColumnTransformer APIs to automate data preprocessing and model training.

This project aims to:

Perform structured data preprocessing

Handle numerical and categorical features separately

Build a reusable machine learning pipeline

Train and evaluate a classification model

Demonstrate how pipelines improve reproducibility and workflow efficiency

#### ⚙️ Methodology / Approach

The project follows a structured machine learning workflow using Scikit-learn.

#### 1️⃣ Data Loading and Inspection

Loaded dataset using Pandas

Inspected missing values

Identified numerical and categorical features

Performed exploratory analysis

#### 2️⃣ Data Preprocessing

The preprocessing was handled using:

SimpleImputer

Median strategy for numerical features

Most frequent strategy for categorical features

StandardScaler for numerical feature scaling

OneHotEncoder for categorical feature encoding

These preprocessing steps were combined using:

ColumnTransformer

#### 3️⃣ Pipeline Construction

A complete pipeline was built

Data preprocessing

Feature transformation

Model training

are executed in a single unified workflow.

#### 4️⃣ Model Training

Dataset split into training and testing sets

Model trained through the pipeline

No manual preprocessing required after pipeline creation

#### 5️⃣ Model Evaluation

Performance was evaluated using:

Accuracy score

Classification report

Confusion matrix (if implemented)

Evaluation was performed directly on the pipeline object

#### 📈 Key Results / Observations

The Scikit-learn Pipeline API simplifies machine learning workflows.

Data preprocessing and model training are seamlessly integrated.

The approach reduces data leakage risks.

The pipeline structure improves reproducibility and maintainability.

The trained model achieves reliable classification performance on unseen test data.

Key Observations:

Both models achieved a very high overall accuracy of **0.96**.

#### For Class 0 (Customer Stayed):
*   Both models show excellent performance with high precision (0.95) and recall (near 1.00), leading to a high f1-score (0.97-0.98).
*   The Random Forest model has a slightly higher recall for this class (1.00) compared to Logistic Regression (0.99), meaning it correctly identified all customers who stayed.

#### For Class 1 (Customer Churned):
*   **Random Forest** has a precision of **1.00** and a recall of **0.87**, resulting in an f1-score of **0.93**.
*   **Logistic Regression** has a precision of **0.97** and a recall of **0.88**, resulting in an f1-score of **0.92**.



🛠 Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib 

#### 📌 Conclusion

*   Both models are highly effective in predicting customer churn, with very similar overall performance.
*   The **Random Forest Classifier** has a perfect precision for predicting churned customers (Class 1), meaning when it predicts a customer will churn, it is always correct. However, its recall for churned customers (0.87) is slightly lower than Logistic Regression, indicating it misses identifying some actual churn cases.
*   The **Logistic Regression** model has a slightly better recall for churned customers (0.88), meaning it identifies a slightly higher proportion of actual churn cases, but with a slightly lower precision (0.97).

Depending on the business objective (e.g., minimizing false positives for churn vs. minimizing false negatives for churn), one model might be marginally preferred over the other. For instance, if avoiding incorrectly flagging a 'staying' customer as 'churned' is critical, Random Forest might be slightly better due to its perfect precision for Class 1. If identifying as many 'churned' customers as possible is the priority, Logistic Regression might have a slight edge due to its slightly higher recall for Class 1.

This project demonstrates how to build a clean, production-style machine learning workflow using Scikit-learn’s Pipeline API. By integrating preprocessing and model training into a single object, the solution becomes scalable, reusable, and less error-prone.
