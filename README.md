# Machine-Learning-Project
Dry Bean Dataset — Complete Machine Learning Analysis

Overview

This project implements a complete Machine Learning workflow using the Dry Bean Dataset. The objective is to explore the dataset, develop predictive models, perform unsupervised clustering, reduce dimensionality, select relevant features, and evaluate different machine learning approaches.

The project covers both supervised and unsupervised learning techniques, along with model evaluation and ensemble learning.

Dataset

The Dry Bean Dataset consists of measurements extracted from images of bean samples. It contains numerical features describing the geometrical and morphological characteristics of beans.

The dataset contains 7 distinct bean varieties:

- Seker
- Barbunya
- Bombay
- Cali
- Dermason
- Horoz
- Sira

Dataset Features

The dataset contains 16 numerical input features and one categorical target variable.

Some of the features include:

- Area
- Perimeter
- Major Axis Length
- Minor Axis Length
- Aspect Ratio
- Eccentricity
- Convex Area
- Equivalent Diameter
- Extent
- Solidity
- Roundness
- Compactness
- Shape Factor 1
- Shape Factor 2
- Shape Factor 3
- Shape Factor 4

Target variable: "Class"

The target variable represents the bean variety and is used for multiclass classification.

Objectives

The primary objectives of this project are:

1. Perform Exploratory Data Analysis (EDA).
2. Develop multiclass classification models.
3. Perform regression analysis.
4. Implement a complete Machine Learning pipeline.
5. Perform unsupervised clustering using K-Means and DBSCAN.
6. Determine the optimal number of clusters for K-Means.
7. Perform feature selection using Scikit-learn techniques.
8. Apply Principal Component Analysis (PCA).
9. Develop classification models using PCA-transformed features.
10. Evaluate models using Stratified K-Fold Cross Validation.
11. Implement Hard Voting and Soft Voting ensemble techniques.
12. Compare model performance across different approaches.

Technologies and Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

Project Workflow

1. Data Loading and Preprocessing

- Load the Dry Bean Dataset.
- Inspect the dataset structure and feature types.
- Identify missing values and duplicate records.
- Perform data cleaning.
- Separate input features and target variable.
- Split data into training and testing sets.

2. Exploratory Data Analysis (EDA)

EDA is performed to understand the structure and characteristics of the dataset.

The analysis includes:

- Dataset dimensions and data types
- Statistical summaries
- Class distribution
- Feature histograms
- Boxplots for outlier detection
- Correlation heatmaps
- Pairwise feature relationships

3. Multiclass Classification

The bean variety is predicted using the numerical input features.

The following classification algorithms are implemented:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree Classifier
- Random Forest Classifier
- Support Vector Machine (SVM)

Models are evaluated using:

- Accuracy
- Precision
- Recall
- Macro-F1 Score
- Confusion Matrix
- Classification Report

4. Regression

Regression is performed by predicting the numerical feature "Area" using the remaining numerical features.

The following regression algorithms are implemented:

- Linear Regression
- Ridge Regression
- KNN Regressor
- Random Forest Regressor

Evaluation metrics include:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

5. Complete Machine Learning Pipeline

A Scikit-learn Pipeline is implemented to combine preprocessing and model development into a single workflow.

The pipeline consists of:

1. Missing-value imputation using median.
2. Feature scaling using StandardScaler.
3. Model training using Random Forest Classifier.
4. Prediction and evaluation.

Pipelines help maintain consistent preprocessing and reduce the risk of data leakage.

6. Unsupervised Learning — K-Means Clustering

K-Means clustering is implemented to group bean samples based on their feature similarities without using class labels during training.

The optimal number of clusters is explored using:

- Elbow Method
- Silhouette Score

The resulting clusters are analyzed and compared with the original bean varieties.

7. Unsupervised Learning — DBSCAN

DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is implemented to identify clusters based on data density.

Parameters explored:

- "eps"
- "min_samples"

The analysis includes:

- Number of clusters identified
- Noise points
- Noise fraction
- Silhouette score where applicable
- Cluster visualization using PCA projection

8. Feature Selection

Feature selection is performed using Scikit-learn techniques to identify the most informative features.

Methods implemented:

- SelectKBest with Mutual Information
- SelectKBest with ANOVA F-score
- Recursive Feature Elimination (RFE)

Selected features are used to develop and evaluate classification models.

9. Principal Component Analysis (PCA)

PCA is applied for dimensionality reduction.

The analysis includes:

- Explained variance ratio
- Cumulative explained variance
- Identification of the number of components required to retain 95% variance
- Two-dimensional PCA visualization

PCA transforms the original features into new orthogonal components while retaining as much variance as possible.

10. Model Development Using PCA

A classification pipeline is developed using PCA-transformed features.

The pipeline includes:

1. Missing-value imputation
2. Standardization
3. PCA retaining 95% explained variance
4. Random Forest classification

The performance is compared with models trained using all features and selected features.

11. Stratified K-Fold Cross Validation

Stratified 5-Fold Cross Validation is used to evaluate model consistency.

The dataset is divided into five folds while approximately preserving class proportions.

Each fold is used once for validation, while the remaining folds are used for training.

The evaluation includes:

- Accuracy
- Macro Precision
- Macro Recall
- Macro-F1 Score
- Mean performance
- Standard deviation

12. Ensemble Learning

Ensemble techniques combine multiple machine learning models to improve predictive performance.

Base models used:

- Logistic Regression
- K-Nearest Neighbors
- Random Forest

Hard Voting — Majority Voting

The final prediction is determined by the majority of predicted class labels from the individual classifiers.

Soft Voting — Probability Voting

The predicted probabilities from individual classifiers are averaged, and the class with the highest average probability is selected.

Both ensemble methods are evaluated and compared.

Model Evaluation and Comparison

The final analysis compares different approaches:

- Individual classification models
- Models trained using all features
- Feature-selected models
- PCA-based models
- Hard Voting ensemble
- Soft Voting ensemble

Classification models are primarily compared using Accuracy and Macro-F1 Score.

Regression models are compared using MAE, RMSE, and R² Score.

Key Concepts Demonstrated

- Supervised Learning
- Unsupervised Learning
- Multiclass Classification
- Regression
- Exploratory Data Analysis
- Data Preprocessing
- Feature Scaling
- Data Leakage Prevention
- Machine Learning Pipelines
- K-Means Clustering
- DBSCAN
- Elbow Method
- Silhouette Analysis
- Feature Selection
- Mutual Information
- ANOVA
- Recursive Feature Elimination
- Principal Component Analysis
- Stratified K-Fold Cross Validation
- Ensemble Learning
- Hard Voting
- Soft Voting
- Model Evaluation

How to Run

Google Colab

1. Download the Jupyter Notebook.
2. Open Google Colab.
3. Upload the ".ipynb" notebook.
4. Execute the cells sequentially or use Runtime → Run all.

The dataset is downloaded automatically within the notebook, so no manual dataset upload is required.

Local Environment

Install the required libraries:

pip install numpy pandas matplotlib seaborn scikit-learn openpyxl jupyter

Launch Jupyter Notebook:

jupyter notebook

Open the notebook and run the cells sequentially.

Conclusion

This project provides an end-to-end implementation of Machine Learning techniques on the Dry Bean Dataset. It explores data analysis, classification, regression, clustering, feature selection, dimensionality reduction, cross-validation, and ensemble learning.

By comparing different algorithms and approaches, the project demonstrates how preprocessing, feature representation, model selection, and evaluation strategies influence machine learning performance.

The notebook serves as a practical demonstration of a complete Machine Learning workflow using Python and Scikit-learn.

---

Project Type: Machine Learning / Data Science
Dataset: Dry Bean Dataset
Language: Python
Environment: Google Colab / Jupyter Notebook
Framework: Scikit-learn
