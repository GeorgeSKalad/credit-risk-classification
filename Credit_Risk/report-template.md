# Module 12 Report Template

## Overview of the Analysis

**Purpose of the Analysis:**

The purpose of this analysis is to build a predictive model for assessing loan risk. Specifically, the analysis aims to predict whether a loan is a "high-risk" or "healthy" loan based on the available financial information. This type of analysis is essential for financial institutions to make informed lending decisions and minimize the risk of defaulting loans.

**Financial Information in the Data:**

The dataset used in this analysis contains financial information related to loans. While the code does not provide a detailed description of the columns in the dataset, it is reasonable to assume that it includes various financial attributes of loan applicants, such as income, credit score, loan amount, and other relevant factors. The critical piece of information for prediction is the "loan_status" column, which indicates whether a loan is considered "high-risk" or "healthy."

**Variables to Predict:**

The primary variable to predict in this analysis is the "loan_status." This variable has two possible values:
- "high-risk": Indicates that the loan is considered high-risk, meaning there is a higher likelihood of default.
- "healthy": Indicates that the loan is healthy, suggesting a lower likelihood of default.

**Stages of the Machine Learning Process:**

The machine learning process in this analysis involves several stages:

1. **Data Loading and Preprocessing:** The code begins by importing necessary libraries and loading the dataset ("lending_data.csv") into a Pandas DataFrame. The data is then split into features (independent variables) and labels (the "loan_status" column). The balance of the labels is checked to assess class imbalance.

2. **Logistic Regression Model (Original Data):** A logistic regression model is created using the original data. The model is trained on the training dataset and then evaluated using the testing dataset. The evaluation includes calculating accuracy, generating a confusion matrix, and printing a classification report.

3. **Resampling Data:** To address class imbalance, the code employs the RandomOverSampler from the imbalanced-learn library to oversample the minority class ("high-risk" loans). This creates a balanced dataset.

4. **Logistic Regression Model (Resampled Data):** A second logistic regression model is created using the resampled data. Like the first model, it is trained and evaluated, with accuracy, confusion matrix, and classification report calculated.

**Methods Used:**

- **Logistic Regression:** Logistic regression is utilized as the predictive model in this analysis. Logistic regression is a common choice for binary classification tasks like this, where the goal is to predict one of two classes.

- **Resampling (RandomOverSampler):** To address class imbalance in the dataset, the RandomOverSampler method from the imbalanced-learn library is applied. This method increases the number of instances in the minority class, making the classes more balanced. This helps improve the model's ability to predict high-risk loans.

Overall, this analysis follows a typical machine learning workflow, starting with data loading and preprocessing, progressing to model creation, and addressing class imbalance through resampling. The primary goal is to predict loan risk, which is crucial for financial institutions to make informed lending decisions and manage their portfolios effectively.

## Results

here are the balanced accuracy scores, precision, and recall scores for the two machine learning models:

**Machine Learning Model 1: (Original Data)**

- Balanced Accuracy Score:
  - Balanced accuracy score of the original model is approximately 0.9944.

- Precision and Recall:
  - For the "high-risk" class:
    - Precision is approximately 0.85.
    - Recall is approximately 0.99.
  - For the "healthy" class:
    - Precision is approximately 0.99.
    - Recall is approximately 0.99.

**Machine Learning Model 2: (Resampled Data)**

- Balanced Accuracy Score:
  - Balanced accuracy score of the resampled model is approximately 0.9944 (same as Model 1).

- Precision and Recall:
  - For the "high-risk" class:
    - Precision is approximately 0.99.
    - Recall is approximately 0.99.
  - For the "healthy" class:
    - Precision is approximately 0.99.
    - Recall is approximately 0.99.

Both machine learning models exhibit excellent balanced accuracy scores, precision, and recall for both classes. The resampling of data in Model 2 does not significantly impact the overall performance metrics compared to Model 1, but it helps address class imbalance, making it a preferred choice for predicting high-risk loans.

## Summary
Both machine learning models, Model 1 (original data) and Model 2 (resampled data), exhibit nearly identical and exceptional predictive performance with balanced accuracy scores around 0.9944. The choice between them depends on specific considerations: Model 1 is computationally efficient and suitable for well-balanced datasets, while Model 2 is recommended when addressing class imbalance is a priority. The decision should align with the specific problem and objectives, whether it's minimizing "high-risk" loans or accurately predicting "healthy" loans.

