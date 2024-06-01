# Fraud Detection

## Description

This repository contains code to analyze credit card transactions and predict whether transactions are fraudulent using machine learning algorithms. The machine learning workflow includes data collection and exploration, data processing, feature correlation analysis, automated processing using pipelines, model building, performance evaluation through cross-validation, and fine-tuning the best-performing model based on precision, recall, and F1 score metrics.

The dataset used in this project is sourced from Kaggle: [Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).

## Table of Contents

- [Installation](#installation)
- [Dataset](#dataset)
- [Data Processing](#data-processing)
- [Feature Selection](#feature-selection)
- [Machine Learning Models](#machine-learning-models)
- [Model Evaluation](#model-evaluation)
- [Fine-Tuning](#fine-tuning)
- [Evaluation on Test Set](#evaluation-on-test-set)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Installation

To work with the code, clone the repository:

```bash
git clone https://github.com/ShayanHodai/fraud-detection.git

## Dataset

![Example Image](images/dataset.png)

# The dataset is highly imbalanced as, less than 1% of total transactions are fraud
![Example Image](images/imbalanced%20dataset.png)

Features histograms: as seen, most features are centred around 0
![Example Image](images/features%20histogram.png)

Time and Amount features need scaling
Time feature is scaled by StandardScaler -> range between 0 to 1
And Amount feature is scaled by RobustScaler -> deals better with outliers
![Example Image](images/two_features.png)

# Random undersampling
To overcome the class imbalance in the dataset and create a balanced dataset, I reduce the number of instances in the majority class. This ensures that the machine learning model can learn to recognize patterns in both classes more effectively.
After undersampling, the shape of the balanced dataset would be (984, 31)

correlation of fraud/normal transactions with non-redundant features
![Example Image](images/corr2.png)

# Machine learning models:
As the cost of False Positive and False Negative in this problem varies, Precision and Recall and, eventually, f1-score are the evaluation metrics of the model performance

Logistic regression:

![Example Image](images/logistic%20regression.png)

KNN:

![Example Image](images/KNN.png)

SVM:

![Example Image](images/SVM.png)

Decision tree classifier, which is highly overfitting:

![Example Image](images/Decision%20Tree.png)

# ROC carve:
![Example Image](images/ROC.png)

# Fine-tuning the best performing model, which is logistic regression:
![Example Image](images/fine-tuning.png)

# Evaluation on the test set:
![Example Image](images/evaluation%20on%20test.png)
