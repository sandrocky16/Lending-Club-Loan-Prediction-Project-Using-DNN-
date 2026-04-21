# 📌 Lending Club Loan Default Prediction using DNN

## 📖 Description
Built a loan default prediction model using Deep Neural Networks (DNN), addressing class imbalance using ADASYN and class weighting. Compared both approaches to improve detection of high-risk borrowers using precision, recall, and F1-score.

## 🧩 Problem Statement
Loan default prediction is a critical challenge for financial institutions, as incorrect risk assessment can lead to significant financial losses. The dataset is highly imbalanced, with fewer defaulters compared to non-defaulters, making it difficult for models to learn minority class patterns. This project aims to build a robust predictive model that accurately identifies potential defaulters while comparing data-level (ADASYN) and algorithm-level (class weighting) imbalance handling techniques.

## 🎯 Objectives
- Predict whether a borrower will default or not
- Handle class imbalance using ADASYN and class weighting
- Compare performance of both techniques in Deep Learning
- Improve recall for the default class

## 🛠️ Approach
- Data cleaning and preprocessing
- Handling missing values and feature selection
- Encoding categorical variables
- Feature scaling using standardization
- Applying ADASYN for oversampling
- Applying class weights in DNN
- Building and training Deep Neural Network models
- Threshold tuning for better recall

## 📊 Results
- Accuracy: 0.77 (replace with your final)
- Recall: Comparable performance for both ADASYN and class weight
- F1-score: Balanced results across both methods

## 💡 Key Insights
- ADASYN improved minority class representation but did not significantly outperform class weighting in DNN
- Class weighting provided similar performance without increasing data size
- Accuracy alone is misleading for imbalanced datasets
- Recall and F1-score are more reliable metrics for evaluating model performance

## 🚀 Business Impact
- Helps financial institutions identify high-risk borrowers
- Reduces loan default risk and financial losses
- Supports better credit decision-making using data-driven insights
