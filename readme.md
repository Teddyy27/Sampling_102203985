# Sampling Techniques and Model Accuracy Analysis

## Overview

This project evaluates the performance of various machine learning models when applied to datasets balanced using different sampling techniques. The objective is to identify the optimal combination of sampling method and machine learning model to achieve the highest accuracy in predicting fraudulent transactions.


## Dataset
- **Input File**: `credit_data.csv`
- **Target Column**: `Class`
- **Features**: All columns except `Class`


## Sampling Techniques Used
The following sampling techniques were applied to balance the dataset:

| Sampling Technique   | Description                                  |
|----------------------|----------------------------------------------|
| **Original**         | No sampling applied.                         |
| **Random OverSampler** | Balances the dataset by randomly duplicating examples in the minority class. |
| **SMOTE**            | Synthetic Minority Over-sampling Technique creates synthetic samples from the minority class. |
| **Random UnderSampler** | Balances the dataset by randomly reducing examples in the majority class. |
| **SMOTEENN**         | A combination of SMOTE and Edited Nearest Neighbors (ENN) for cleaning noisy data. |

## Models Applied

Multiple machine learning models were evaluated to determine their efficacy in fraud detection:

- **Random Forest**
- **Logistic Regression**
- **SVM (Support Vector Machine)**
- **KNN (K-Nearest Neighbors)**
- **Gradient Boosting**

## Model Accuracy Results

The performance of each model across different sampling techniques is summarized in the table below, which highlights the robustness of each model under varied data conditions:


| Sampling Technique       | Random Forest | Logistic Regression | SVM    | KNN    | Gradient Boosting |
|--------------------------|---------------|---------------------|--------|--------|-------------------|
| **Original**             | 91.20%        | 86.34%              | 90.50% | 88.75% | 89.45%            |
| **Random OverSampler**   | 93.45%        | 88.20%              | 92.10% | 90.30% | 91.60%            |
| **SMOTE**                | 94.10%        | 89.00%              | 93.55% | 91.25% | 92.75%            |
| **Random UnderSampler**  | 90.85%        | 85.75%              | 89.65% | 87.55% | 88.20%            |
| **SMOTEENN**             | 92.30%        | 87.45%              | 91.20% | 89.90% | 90.55%            |

## Instructions for Reproduction
To reproduce the analysis, follow these steps:

1. Install dependencies:
   ```bash
   pip install pandas scikit-learn imbalanced-learn matplotlib

### 2. Prepare the Dataset

- **Place the `credit_data.csv` file in your working directory.** Ensure that this file is in the same directory as your Python scripts to facilitate easy access by the script.

### 3. Run the Analysis

- **Execute the provided Python script.** If you are using the command line, navigate to your project directory and run:
- Replace your_script_name.py with the name of your script file.

   ```bash
      python your_script_name.py

### 4. View the Outputs

- Observe the outputs displayed in the console. These outputs will include the performance metrics of the models used.
- Reproducibility: Adjust the random states in the script to maintain reproducibility of the results.
