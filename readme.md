# Sampling Techniques and Model Accuracy Analysis

## Overview

This project explores various sampling techniques applied to a highly imbalanced dataset to understand their impact on model performance. The original dataset consisted of 763 non-fraudulent cases and only 9 fraudulent cases, presenting a challenge typical in fraud detection scenarios. By employing oversampling and other sampling methods, the dataset was balanced, allowing for a fair evaluation of multiple machine learning models.

## Dataset

The dataset features transactions from credit card users, where the majority are legitimate transactions with a small fraction of fraudulent activities. It includes features related to transaction details such as amount, time, and anonymized attributes.

## Sampling Techniques Used

Five distinct sampling techniques were employed to create diverse training environments for the models:

1. **Simple Random Sampling**: Random selection without replacement, providing an unbiased representation of the population.
2. **Systematic Sampling**: Samples are drawn at regular intervals, ensuring no clustering and reducing the risk of bias.
3. **Cluster Sampling**: Involves partitioning the data into clusters, and then a simple random sample of these clusters is selected.
4. **Stratified Sampling**: Stratifies the population into homogeneous subgroups before sampling, ensuring that each subgroup is adequately represented.
5. **Bootstrap Sampling**: Samples are drawn with replacement from the dataset, allowing for larger samples and extensive training.

## Models Applied

Multiple machine learning models were evaluated to determine their efficacy in fraud detection:

- **Random Forest**
- **Logistic Regression**
- **SVM (Support Vector Machine)**
- **KNN (K-Nearest Neighbors)**
- **Gradient Boosting**

## Model Accuracy Results

The performance of each model across different sampling techniques is summarized in the table below, which highlights the robustness of each model under varied data conditions:

```markdown
| Sampling Technique        | Random Forest | Logistic Regression | SVM    | KNN    | Gradient Boosting |
|---------------------------|:-------------:|:-------------------:|:------:|:------:|:-----------------:|
| **Simple Random Sampling**| **100.00%**   | 80.52%              | 96.10% | 97.40% | 96.10%            |
| **Systematic Sampling**   | 99.34%        | 90.79%              | **99.34%** | 97.37% | **98.03%**          |
| **Cluster Sampling**      | 99.34%        | 90.79%              | **99.34%** | 97.37% | **98.03%**          |
| **Stratified Sampling**   | 99.34%        | 90.79%              | **99.34%** | 97.37% | **98.03%**          |
| **Bootstrap Sampling**    | 99.34%        | 90.79%              | **99.34%** | 97.37% | **98.03%**          |
