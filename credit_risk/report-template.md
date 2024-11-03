# Module 12 Report Template

### Overview of the Analysis

The purpose of this analysis was to develop a machine learning model that could predict loan risk, specifically classifying loans as either “healthy” (0) or “high-risk” (1). Accurately predicting loan status is essential for financial institutions to make informed lending decisions and mitigate potential risks. By analyzing historical loan data, we aim to train a model capable of identifying high-risk loans to prevent defaults.

#### Financial Information in the Data

The dataset, provided in the `lending_data.csv` file, includes various financial features for each loan, such as:
- **Loan Size**: The amount of money loaned.
- **Interest Rate**: The percentage charged on the loan.
- **Borrower Income**: The borrower’s income.
- **Debt-to-Income Ratio**: A financial ratio indicating the percentage of income going toward debt payments.
- **Number of Accounts**: The number of accounts the borrower has.
- **Derogatory Marks**: Negative marks on the borrower’s credit.
- **Total Debt**: The total debt amount owed by the borrower.

The target variable, **`loan_status`**, was either `0` (indicating a healthy loan) or `1` (indicating a high-risk loan). A `value_counts` check on this variable would confirm class distribution, showing whether the dataset is balanced or imbalanced.

#### Machine Learning Process

The analysis followed these key steps in the machine learning pipeline:
1. **Data Preparation**: Loading the data, defining `X` (features) and `y` (target) variables, and splitting the dataset into training and testing sets. This split allows the model to train on one subset and be evaluated on unseen data, providing a robust test of model generalizability.
2. **Model Selection**: We used the **Logistic Regression** algorithm as our primary model due to its effectiveness in binary classification tasks and its interpretability in predicting probability-based outcomes.
3. **Model Training**: The Logistic Regression model was trained on the training dataset, allowing it to learn relationships between features and the target variable.
4. **Model Evaluation**: The model’s performance was evaluated using a confusion matrix and classification report. These metrics provided insight into the model's accuracy, precision, and recall for both loan classes.

The primary machine learning method used in this analysis was **Logistic Regression**, given its suitability for binary classification. Additional models could be explored in future iterations to improve predictive power, particularly if the dataset is imbalanced.


### Results

* **Machine Learning Model 1: Logistic Regression**
    * **Accuracy**: The model achieved an accuracy of **99%**, indicating a strong overall performance with only a small proportion of loans misclassified.
    * **Precision**:
      - **Class 0 (Healthy Loans)**: Precision is **1.00**, meaning all loans predicted as healthy are almost certainly healthy.
      - **Class 1 (High-Risk Loans)**: Precision is **0.86**, showing that 86% of loans predicted as high-risk were indeed high-risk. This is a reliable precision score for high-risk loans.
    * **Recall**:
      - **Class 0 (Healthy Loans)**: Recall is **0.99**, indicating that nearly all healthy loans were correctly identified.
      - **Class 1 (High-Risk Loans)**: Recall is **0.94**, showing that 94% of actual high-risk loans were successfully detected, which is crucial for minimizing missed high-risk cases.
    * **F1-Score**:
      - **Class 0 (Healthy Loans)**: F1-score is **1.00**.
      - **Class 1 (High-Risk Loans)**: F1-score is **0.90**, reflecting a strong balance between precision and recall for high-risk loan predictions.

Overall, the model provides reliable predictions across both classes, with particularly high recall for high-risk loans, making it suitable for effective risk management.


### Summary of Machine Learning Model Performance: Logistic Regression

#### Model Overview
The Logistic Regression model demonstrates impressive performance metrics for predicting loan status, classifying loans into healthy (Class 0) and high-risk (Class 1) categories.

#### Performance Metrics

1. **Accuracy**: 
   - The model achieved an accuracy of **99%**, indicating a strong overall performance with only a small proportion of loans misclassified.

2. **Precision**:
   - **Class 0 (Healthy Loans)**: 
     - Precision is **1.00**, meaning all loans predicted as healthy are almost certainly healthy.
   - **Class 1 (High-Risk Loans)**: 
     - Precision is **0.86**, indicating that 86% of loans predicted as high-risk were indeed high-risk. This precision score is reliable for high-risk loans.

3. **Recall**:
   - **Class 0 (Healthy Loans)**: 
     - Recall is **0.99**, indicating that nearly all healthy loans were correctly identified.
   - **Class 1 (High-Risk Loans)**: 
     - Recall is **0.94**, showing that 94% of actual high-risk loans were successfully detected. This is crucial for minimizing missed high-risk cases.

4. **F1-Score**:
   - **Class 0 (Healthy Loans)**: 
     - F1-score is **1.00**, indicating perfect balance for healthy loans.
   - **Class 1 (High-Risk Loans)**: 
     - F1-score is **0.90**, reflecting a strong balance between precision and recall for high-risk loan predictions.

### Model Recommendation

1. **Best Performing Model**:
   - The **Logistic Regression** model appears to perform the best overall based on the provided metrics. Its high accuracy, perfect precision for healthy loans, and strong precision and recall for high-risk loans make it a reliable choice for this classification task.

2. **Performance Context**:
   - The performance of the model is context-dependent. In the context of loan approval, accurately identifying high-risk loans (Class 1) is crucial. The high recall (0.94) means that the model successfully identifies a majority of high-risk cases, which is essential for minimizing financial losses associated with defaults. Therefore, while the model performs well in general, prioritizing performance on high-risk loans is critical, especially in risk management scenarios.

3. **Final Recommendation**:
   - Given the robust performance metrics, particularly for high-risk loans, it is recommended to **use the Logistic Regression model** for predicting loan statuses. However, continuous monitoring and potential adjustments should be made to maintain or improve performance, especially for high-risk loan detection, as new data becomes available. 

### Conclusion
The Logistic Regression model is highly effective for classifying loans as healthy or high-risk, providing a strong foundation for risk assessment in lending. With its exceptional accuracy and reliability in predicting high-risk loans, it serves as a solid choice for financial institutions aiming to enhance their lending decision processes.




