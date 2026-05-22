# 📌 Lending Club Loan Default Prediction using Deep Neural Networks (DNN)

## 📖 Description

### Developed a loan default prediction system using a Deep Neural Network (DNN) to identify high-risk borrowers in the Lending Club dataset. Since the dataset was highly imbalanced with fewer defaulter cases, imbalance-### handling techniques such as ADASYN and class weighting were applied and compared.

### The project focused on improving detection of defaulters using recall, precision, and F1-score rather than relying solely on accuracy, since financial risk prediction requires stronger minority-class detection.

## 🧩 Problem Statement

### Loan default prediction is a major challenge in the financial sector because incorrect risk assessment can lead to substantial financial losses.

### The Lending Club dataset contained significantly fewer ‘Unpaid’ (default) cases compared to ‘Paid’ loans, causing severe class imbalance.

### Traditional deep learning models tend to favor the majority class, resulting in poor detection of risky borrowers. Therefore, the objective of this project was to build a robust Deep Neural Network capable of ### identifying potential defaulters effectively while comparing:

### Data-level imbalance handling using ADASYN

### Algorithm-level imbalance handling using Class Weights

## 🎯 Objectives

### 1. Predict whether a borrower will default or repay the loan

### 1. Handle class imbalance using ADASYN and class weighting

### 2. Compare both imbalance-handling approaches in DNN

### 3. Improve recall for the default class

### 4. Optimize classification threshold for better risk detection

### 5. Build a generalized ANN model with stable performance on unseen data

🛠️ Approach
Performed data cleaning and preprocessing
Handled missing values and removed irrelevant features
Encoded categorical variables
Applied feature scaling using standardization
Split the dataset into training, evaluation, and test sets
Applied ADASYN oversampling for minority-class generation
Applied class weighting during DNN training
Built a Deep Neural Network with:
Dense hidden layers
ReLU activation
Dropout regularization
Used Early Stopping to prevent overfitting
Performed threshold tuning for improved recall
Compared ADASYN and class-weighted models using classification metrics
📊 Results
🔹 ADASYN-Based DNN Model

Threshold Used: 0.38

Metric	Unpaid (Class 1)
Precision	~0.23–0.25
Recall	~0.54–0.55
F1-score	~0.32–0.34
Accuracy	~0.64–0.65
Observation

ADASYN improved minority-class learning by generating synthetic defaulter samples, allowing the model to identify more risky borrowers.

However, the aggressive oversampling increased false positives, which reduced precision and caused the model to classify many safe borrowers as risky applicants.

Despite lower precision, the model showed stable generalization across evaluation and test datasets.

🔹 Class Weight-Based DNN Model (Final Model)

Class Weights Used: class_weight = {0:1, 1:5}
Threshold Used: 0.38

Metric	Unpaid (Class 1)
Precision	~0.24–0.25
Recall	~0.60–0.66
F1-score	~0.34–0.36
Accuracy	~0.62
Observation

Class weighting improved recall more effectively than ADASYN while maintaining slightly better F1-score and stable minority-class learning.

Unlike ADASYN, class weighting improved defaulter detection without generating synthetic samples, resulting in better generalization and more balanced performance.

Therefore, the class-weighted DNN model was selected as the final model for the project.

💡 Key Insights
The Lending Club dataset exhibited severe class imbalance, making default prediction challenging.
ADASYN improved minority-class detection by generating synthetic samples for defaulters.
Although ADASYN improved recall, it introduced excessive false positives and reduced precision.
Class weighting improved recall more effectively while avoiding synthetic data generation.
The class-weighted model achieved better F1-score and more stable generalization performance.
Lowering the classification threshold from 0.5 to 0.38 significantly improved recall for detecting risky borrowers.
Accuracy alone was misleading because of class imbalance.
Recall and F1-score were more meaningful evaluation metrics for financial risk prediction.
Similar evaluation and test performance indicated that the final model generalized well without significant overfitting.
🚀 Business Impact
Helps financial institutions identify high-risk borrowers before loan approval
Reduces financial losses caused by loan defaults
Supports data-driven and risk-aware lending decisions
Improves borrower screening by prioritizing detection of potential defaulters
Demonstrates how imbalance handling and threshold tuning improve real-world financial risk prediction systems
Enables lenders to reduce exposure to risky loans while maintaining scalable automated decision-making systems
