**Name: Prakhar Bhardwaj**\
**Reg No: 23MEI10051**\
**Application no: IN26011412**\
**Batch Number: 1(A)**

# AI-ML-Assignment-4
# Breast Cancer Tumor Classification using K-Nearest Neighbors (KNN)

## Objective
The objective of this project is to develop a machine learning model for a healthcare organization to predict whether a breast tumor is **Malignant (M)** or **Benign (B)** based on diagnostic measurements. We implemented a K-Nearest Neighbors (KNN) classification model to achieve accurate tumor classification, which can assist medical professionals in diagnosis.

## Dataset Link
**Breast Cancer Wisconsin Diagnostic Dataset**  
Source: [Kaggle - Breast Cancer Wisconsin Data](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)

## Libraries Used
*   **Pandas:** For data loading, manipulation, and analysis.
*   **Scikit-learn:** For data preprocessing (StandardScaler), splitting the dataset, model building (KNeighborsClassifier), and evaluation metrics.
*   **Matplotlib & Seaborn:** For generating data visualizations, specifically the confusion matrix heatmap.

## Methodology
The project follows a standard machine learning pipeline:

1.  **Data Understanding & Loading:** 
    *   Loaded the dataset using Pandas.
    *   Identified the target variable (`diagnosis`) and the 30 numerical diagnostic features.
2.  **Data Preprocessing:**
    *   Cleaned the dataset by removing unnecessary columns (`id` and the empty `Unnamed: 32` column).
    *   Encoded the target labels (Malignant = 1, Benign = 0).
    *   **Feature Scaling:** Standardized the features using `StandardScaler` so that all numerical values have a mean of 0 and a standard deviation of 1. This is a crucial step for distance-based algorithms like KNN.
    *   Split the data into training (80%) and testing (20%) sets.
3.  **Model Development:**
    *   Initialized a K-Nearest Neighbors classifier with `K=5`.
    *   Trained the model on the scaled training dataset.
4.  **Model Evaluation:**
    *   Generated predictions on the test set.
    *   Evaluated performance using Accuracy, Precision, Recall, F1-Score, and a Confusion Matrix.

## Results
The KNN model demonstrated excellent performance in classifying tumors. Typical results on the test set include:
*   **Accuracy:** ~95% - 97%
*   **Precision:** Highly precise, meaning very few false positive alarms.
*   **Recall:** Exceptional recall (>90%), successfully identifying the vast majority of true malignant cases, which is the most critical metric in this medical context to avoid false negatives.
*   **Confusion Matrix:** Visually confirmed that the model effectively separates the Malignant and Benign classes with minimal misclassifications.

## Conclusion
The K-Nearest Neighbors model is highly effective at classifying breast cancer tumors using cell nucleus measurements. 

A critical finding in this methodology is the absolute necessity of **feature scaling**. Because KNN calculates the Euclidean distance between data points to make predictions, features with large numeric ranges (e.g., cell area) would completely dominate the distance metric and overshadow smaller-scale features (e.g., cell smoothness) if the data was not standardized.

While highly accurate, one **limitation of the KNN algorithm** is that it is a "lazy learner." It does not mathematically generalize the data during a training phase; instead, it memorizes the entire dataset. For very large medical datasets, this makes the prediction phase significantly slower and more memory-intensive, as it must compute the distance to every existing patient record for each new diagnosis.
