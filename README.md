# Credit Risk Classification: Machine Learning 
## Module 20 Challenge 

![download](https://github.com/CBURKHARDT47/Credit-Risk-Classification-/assets/128064003/1a6d2034-b9cd-4988-8e27-3a7ed38a2e66)

### Business Context
Credit scoring aids lenders in the granting of consumer credit. Typical application areas in the consumer market include: creditcards, autoloans, home loans and a wide variety of personal loan products.

Objective
In this case study, one of the leading banks would like to predict customers who are most likely to default on the loan. For new customers we need to decide whether to extend credit or not by analyzing the behaviour of existing customers. Various machine learning techniques are used to train and evaluate a model that can identify the creditworthiness of borrowers based on loan risk, using a dataset of historical lending activity from a peer-to-peer lending services company.

### The instructions for this Challenge are divided into the following subsections:  
* Split the Data into Training and Testing Sets
* Create a Logistic Regression Model with the Original Data
* Write a Credit Risk Analysis Report

Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:
* Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
* Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
* NOTE: A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
* Split the data into training and testing datasets by using train_test_split.

Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:
* Fit a logistic regression model by using the training data (X_train and y_train).
* Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
* Evaluate the model’s performance by doing the following:
    * Generate a confusion matrix.
    * Print the classification report.
* Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

Write a Credit Risk Analysis Report
Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository. Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:
* An overview of the analysis: Explain the purpose of this analysis.
* The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.
* A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.
