# Credit Risk Analysis Report

### Objective: 
    The main objective of this analysis is to build and evaluate machine learning models that can predict whether a borrower is low-risk or high-risk based on various factors related to lending activity. The analysis aims to assess the risk associated with lending to borrowers.  

### Purpose: 
The analysis contributes to the development of a credit scoring system. By classifying borrowers into low-risk and high-risk categories, the lending company can make more informed decisions about approving or denying loan applications. It addresses the challenge of class imbalance and aims to strike a balance between approving loans to creditworthy borrowers and minimizing the risk associated with lending to high-risk borrowers.

### Data and Features:

    * The dataset contains historical lending activity data from a peer-to-peer lending services company.
    * The features used for analysis include loan size, interest rate, borrower's income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. 

### Data Split: 

    * The dataset was split into a training set and a testing set.
    * The training set (X_train and y_train was used to build the initial logistic regression model (Logistic Regression Model 1). 
    * The testing set was used to evaluate the model's performance. The purpose of the model was to determine whether a loan to the borrower in the testing set would be low- or high-risk and results are summarized below.


### Imbalanced Data:

    * The original dataset had a significant class imbalance, with 75,036 low-risk loan data points and only 2,500 high-risk data points.
    * To address this imbalance, the training data was resampled using the RandomOverSampler from imbalanced-learn to generate equal numbers of low-risk and high-risk data points, resulting in 56,277 data points for each class.
    * The purpose of Logistic Regression Model 2 was to determine whether a loan to the borrower in the testing set would be low- or high-risk. The results are summarized below.

### Model Evaluation:

Logistic Regression Model 1 was evaluated with the following metrics:
        * Precision: 93% (average)
            ** Precision for low-risk loans: 100%
            ** Precision for high-risk loans: 87%
        * Accuracy: 94%
        * Recall: 95% (average)
            ** Recall for low-risk loans: 100%
            ** Recall for high-risk loans: 89%

Logistic Regression Model 2, trained on the resampled data, was evaluated with the following metrics:
        * Precision: 93% (average)
            ** Precision for low-risk loans: 100%
            ** Precision for high-risk loans: 87%
        * Accuracy: 100%
        * Recall: 100% (average)
            ** Recall for low-risk loans: 100%
            ** Recall for high-risk loans: 100%


    Class 0 (low-risk loans): 75,036 instances
    Class 1 (high-risk loans): 2,500 instances

This information gives you an overview of the distribution of the target variable in your dataset. It shows that there are significantly more instances of low-risk loans (class 0) compared to high-risk loans (class 1). The class distribution is highly imbalanced, which is a common scenario in credit risk assessment.

### Summary Interpretation of Results:

    Both Logistic Regression Model 1 and Model 2 exhibit high precision, accuracy, and recall for predicting low-risk loans, with perfect performance in some cases. For high-risk loans, the models achieved a lower precision but still demonstrated a reasonably high recall. Model 2, which was trained on resampled data, achieved perfect accuracy and recall for both low-risk and high-risk loans, indicating excellent performance on the testing set. The analysis suggests that the logistic regression models, especially Model 2 with resampled data, are effective at identifying low-risk loans. While the precision for high-risk loans is slightly lower, the models excel in recall, meaning they can effectively identify a high proportion of high-risk loans. 

     Overall, the results indicate that logistic regression models can be valuable tools for assessing the creditworthiness of borrowers in this context, particularly when addressing imbalanced datasets through resampling techniques like RandomOverSampler. Further evaluation and validation, possibly with additional datasets, would be beneficial to confirm the models' performance and generalizability. If requested, I would recommend using Model 2 due to its 100% accuracy. The model fitted with imbalanced data has a higher possibility of making these mistakes: 

  * a healthy loan (low-risk) is classified as a non-healthy loan (high-risk).
  * a non-healthy loan (high-risk) is classified as a healthy loan (low-risk). 

In many real-world machine learning problems, the relative importance of correctly predicting each class is not equal, and it depends on the goals and consequences associated with the predictions. We will need a model to be as accurate as possible when diagnosing medical conditions or detecting fradulent transactions, for example. An overfit model may perform well on the training data but is of limited practical use if it cannot make accurate predictions on real-world examples.

