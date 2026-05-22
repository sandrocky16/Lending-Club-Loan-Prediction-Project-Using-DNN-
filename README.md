# 📌 Lending Club Loan Default Prediction using Deep Neural Networks (DNN)

📖 Description

Developed a loan default prediction system using a Deep Neural Network (DNN) to identify high-risk borrowers in the Lending Club dataset. Since the dataset was highly imbalanced with fewer defaulter cases, imbalance handling techniques such as ADASYN and class weighting were applied and compared. The project focused on improving detection of defaulters using recall, precision, and F1-score rather than relying solely on accuracy.

🧩 Problem Statement

Loan default prediction is a major challenge in the financial sector because incorrect risk assessment can lead to substantial financial losses. The Lending Club dataset contained significantly fewer 'Unpaid' (default) cases compared to 'Paid' loans, causing severe class imbalance.

Traditional models tend to favor the majority class, resulting in poor detection of risky borrowers. Therefore, the objective of this project was to build a robust deep learning model capable of identifying potential defaulters effectively while comparing:

Data-level imbalance handling using ADASYN
Algorithm-level imbalance handling using class weights

🎯 Objectives

Predict whether a borrower will default or repay the loan
Handle class imbalance using ADASYN and class weighting
Compare both imbalance-handling approaches in DNN
Improve recall for the default class
Optimize classification threshold for better risk detection

🛠️ Approach

Performed data cleaning and preprocessing
Handled missing values and removed irrelevant features
Encoded categorical variables
Applied feature scaling using standardization
Split the dataset into training, evaluation, and test sets
Applied ADASYN oversampling for minority class generation
Applied class weighting in DNN training
Built a Deep Neural Network with:
Dense hidden layers
ReLU activation
Dropout regularization
Used Early Stopping to prevent overfitting
Performed threshold tuning for improved recall

📊 Results

🔹 ADASYN-Based Model
Metric	Unpaid (Class 1)
Precision	~0.23
Recall	~0.60
F1-score	~0.33
Accuracy	~0.62
Observation

ADASYN significantly improved recall for defaulters but introduced a large number of false positives, reducing precision.

🔹 Class Weight-Based DNN Model (Final Model)

Threshold used: 0.45

Metric	Unpaid (Class 1)
Precision	~0.25
Recall	~0.63
F1-score	~0.36
Accuracy	~0.63
Observation

Class weighting provided more stable and balanced performance while maintaining strong recall for identifying risky borrowers.

💡 Key Insights

ADASYN improved minority-class detection but increased false positives due to aggressive oversampling.
Class weighting achieved better balance between precision and recall without generating synthetic data.
Combining ADASYN with class weights caused overcompensation toward the minority class and degraded performance.
Lowering the classification threshold from 0.5 to 0.45 improved recall for defaulters significantly.
Accuracy alone was misleading because of dataset imbalance.
Recall and F1-score were more meaningful evaluation metrics for this financial risk prediction problem.

🚀 Business Impact

Helps financial institutions identify high-risk borrowers before loan approval
Reduces financial losses caused by loan defaults
Supports risk-aware lending decisions using data-driven insights
Improves borrower screening by prioritizing detection of potential defaulters
Demonstrates how threshold tuning and imbalance handling can improve real-world financial risk prediction systems
