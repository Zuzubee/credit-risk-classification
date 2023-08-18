# Module 20 Report


## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.

    * **The purpose of this analysis is to train and evaluate a model based on loan risk in order to identify the reliability of borrowers or mortgagors.**


* Explain what financial information the data was on, and what you needed to predict.
    * **The financial data described loan details like loan size, interest rate, borrower income, loan status, etc. In order to create a prediction, the data was split into training and testing datasets, a logistic regression model was created, the model was fit using training data, and then `.predict()` was used on the test data.**


* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
    * **The `y` values, or loan status of individuals in the dataset are what we want to predict. In this case, `0` indicates a healthy loan while `1` indicates a high risk loan. the `.value_counts()` tells us that there are `75036` healthy loans and `2500` high risk loans in this dataset.**


* Describe the stages of the machine learning process you went through as part of this analysis.
    * **To start, the data was split into training and testing sets, next, `X` and `y` variables were created and the data was split using `train_test_split()`, then a logistic regression model was created with the original data and fit using the training data. Predictions were made next and then the models performance was tested by calculating the `accuracy score`, generating a `confusion matrix`, and printing a `classification report`. After this, a logistic regression model was predicted with resampled training data using the `RandomOverSampler()` module and repeating the previous process, only this time using that resampled data.**


* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
    * **The logistic regression module was used to aid predictions throughout the analysis, and the `RandomOverSampler()` was used to create resampled data. This allowed the original training data to be fit to the newly created model where further predictions and performance could be evaluated.**

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning ***`Model 1`***:

    * Description of ***`Model 1`*** `Accuracy`, `Precision`, and `Recall` scores.
    
    * Balanced Accuracy score: `95% or 0.952` which is good!
    
    * Accuracy Score: `99% or 0.992` which is really good!
        
    * `Precison` for healthy loans is `100%` and for high-risk loan is `85%`.
    
    * `Recall` for healthy loans is `99%` and for high-risk loan is `91%`
    
    * `F1score` for healthy loans is `100%` and for high-risk loan is `88%`.
    
    * Healthy loans see ideal `precision` and `f1-scores` at `100%`, while recall is at `99%`.
    
    * High-risk loans' precision is `15%` lower than healthy loans
    
    * High-risk loans are also at lower `recall` and `f1-score` values than the healthy loans with `8%` and `2%` variations (respectively)


* Machine Learning ***`Model 2`***:
    * Description of ***`Model 2`*** `Accuracy`, `Precision`, and `Recall` scores.
    
    * Balanced Accuracy score: `99% or 0.994` which is really good!
    
    * Accuracy score: `99% or 0.994` which is also really good!
    
    * `Precison` for healthy loans is `100%` and for high-risk loan is `84%`.
    
    * `Recall` for healthy loans is `99%` and for high-risk loan is `99%`
    
    * `F1score` for healthy loans is `100%` and for high-risk loan is `91%`.
    
    * High-risk loans experienced general increase in `recall` and `f1-score`- `8%` and `3%` (respectively)
    
    * High-risk loans experienced a decrease in precision by `1%`.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
    * **It seems that Machine Learning *`Model 2`* performs the best because we see a general increase in recall and f1 scores, and even the macro average. Accuracy is at `99%` for both models, but if one must choose, then the inceases do indicate *`Model 2`* as the better performing model.**

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
    * **It is important to predict both the ones and zeros in order to determine a the creditworthiness of borrowers. Being able to compare the two allows for well-rounded predictions and conclusions to be made.**