# Module 12 Report Template

## Overview of the Analysis

### Purpose of the Analysis

The purpose of this analysis is to develop machine learning models to predict loan statuses based on financial data. The goal is to assess the performance of these models in predicting whether a loan is "healthy" (low-risk) or "high-risk" based on various financial features.

### Financial Information and Prediction Target

The financial data used in this analysis includes information about loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The prediction target is the "loan_status" variable, where 0 represents healthy loans (low-risk) and 1 represents high-risk loans.

### Basic Information about Variables

- The dataset contains 75,036 instances of healthy loans (0) and 2,500 instances of high-risk loans (1). This indicates a class imbalance, with significantly more healthy loans than high-risk loans.

### Stages of the Machine Learning Process

The machine learning process involved the following stages:

1. **Data Preprocessing:** The dataset was read into a Pandas DataFrame, and the data was split into labels (y) and features (X). The class imbalance was identified, and the data was divided into training and testing sets.

2. **Logistic Regression Model with Original Data:** A logistic regression model (Model 1) was created and trained using the original imbalanced data. The model's performance was assessed using balanced accuracy, precision, and recall scores.

3. **Logistic Regression Model with Resampled Data:** The training data was oversampled using the RandomOverSampler to balance the classes. A new logistic regression model (Model 2) was trained using the oversampled data, and its performance was evaluated using the same metrics.

### Methods Used

- **Logistic Regression:** Logistic regression was used as the primary classification algorithm to predict loan statuses.
- **RandomOverSampler:** Random oversampling was employed to address the class imbalance in the training data.

## Results

### Machine Learning Model 1:

- Balanced Accuracy Score: 95.20%
- Precision for High-Risk Loans (1): 85%
- Recall for High-Risk Loans (1): 91%

### Machine Learning Model 2:

- Balanced Accuracy Score: 99.37%
- Precision for High-Risk Loans (1): 99%
- Recall for High-Risk Loans (1): 99%

## Summary

The results of the machine learning models are as follows:

- **Machine Learning Model 1:** This model, trained with the original imbalanced data, achieved a reasonably good balanced accuracy score of 95.20%. However, its precision and recall for high-risk loans (1) were lower, indicating that it struggles to predict high-risk loans effectively.

- **Machine Learning Model 2:** After applying random oversampling to balance the classes in the training data, Model 2 demonstrated significantly improved performance. It achieved an impressive balanced accuracy score of 99.37%, along with high precision and recall scores for high-risk loans (1). This model outperforms Model 1 in terms of predicting high-risk loans.

**Recommendation:**

- Model 2, trained with the resampled data, is the recommended model for predicting loan statuses. It outperforms Model 1 in terms of balanced accuracy, precision, and recall, particularly for high-risk loans. 

- Performance may depend on the specific problem you are trying to solve. If the primary concern is correctly identifying high-risk loans (1), Model 2 is the better choice. However, if overall accuracy is more critical and the class imbalance can be managed through other means, Model 1 could still be considered.

In summary, Model 2 is the preferred choice for this task due to its superior performance in predicting high-risk loans while maintaining high accuracy overall.
