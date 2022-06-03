# Module 12 Report Template

## Overview of the Analysis

* Explain the purpose of the analysis.
The purpose of the analysis was to build a model from data with imbalanced classes to help determine creditworthiness of a borrower.  

* Explain what financial information the data was on, and what you needed to predict.
The financial data information was based off historical lending activity to help predict creditworthiness of a borrower. 

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
Used `value_counts` to determine the balance of the labels variable `y`.



* Describe the stages of the machine learning process you went through as part of this analysis.
1- Split the Data into Training and Testing Sets
    1- Read the data
    2- Create the labels
    3- Check the balance of the labels
    4- Split the data
    
2- Created a Logistic Regression Model with the Original Data.
    1- Fit model by using the original data
    2- Save the predictions
    3- Evaluate performance
    
3- Predict a Logistic Regression Model with Resampled Training Data
    1- Resample the data 
    2- Fit the model using resampled training data
    3- Evaluate performance
        1- Calculate the accuracy score of the model.
        2- Generate a confusion matrix.
        3- Print the classification report.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
Use the `RandomOverSampler` module from the imbalanced-learn library to resample the data.
Use the `LogisticRegression` classifier and the resampled data to fit the model and make predictions.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
    * Accuracy  |   0.9520479254722232
    * Precision |   0.85 
    * Recall    |   0.99


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
    * Accuracy  |   0.9947308560359689
    * Precision |   0.99
    * Recall    |   0.99
    
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
It appears the oversampled data model performed best. With both precision and recall being 99%.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
Its most important to focus on precision to determine fasle positives or borrowers that qualified but defaulted. However, Its also important to focus on the recall or 0's. Recall represents False Negatives. False negatives represent borrowers that should have qualified but did not.  This is a loss to the lender. 
