# Credit Risk Analysis

## Overview
The purpose of the analysis is to find a predictive model that balances precision and sensitivity (recall) in the data, and thereby reduces the chance of predicting too many high or low risk results in the analysis.

The credit risk analysis examines data from LendingClub, a peer-to-peer lending service company. Credit risk is an unbalanced classification problem, because good loans easily outnumber risky loans. Therefore, the research department has been tasked with employing different machine learning techniques to train and evaluate models using resampling.

This analysis will use the LoanStats_2019Q1.csv dataset, and imbalanced-learn and scikit-learn libraries to perform the analysis. The following models will be used in the analysis:
* Naive Random Oversampling
* SMOTE Oversampling
* Cluster Centroid Undersampling
* SMOTEENN Sampling
* Balanced Random Forest Classifying
* Easy Ensemble Classifying

## Results
For each model, a summative report shows the accuracy score, confusion matrix and classification report displayed below. These scores are key indicators to determine a balance between precision and sensitivity that will help eliminate false positives and negatives. 

### Naive Random OverSampling
* Accuracy score: 66%
* Precision (High risk): 1%
* Precision (Low risk): 100%
* Recall (High risk): 72%
* Recall (low risk): 60%

<img src="images/random_oversampling_report.png" width="50%" height="20%">

### SMOTE Oversampling
* Accuracy score: 66%
* Precision (High risk): 1%
* Precision (Low risk): 100%
* Recall (High risk): 62%
* Recall (low risk): 69%

<img src="images/smote_oversampling_report.png" width="50%" height="30%">

### ClusterCentroid Undersampling
* Accuracy score: 54%
* Precision (High risk): 1%
* Precision (Low risk): 100%
* Recall (High risk): 69%
* Recall (low risk): 40%

<img src="images/clustercentroid_undersampling_report.png" width="50%" height="30%">

### SMOTEEN Sampling
* Accuracy score: 67%
* Precision (High risk): 1%
* Precision (Low risk): 100%
* Recall (High risk): 77%
* Recall (low risk): 57%

<img src="images/smoteen_report.png" width="50%" height="30%">

### Balanced Random Forest Classifying
* Accuracy score: 68%
* Precision (High risk): 88%
* Precision (Low risk): 100%
* Recall (High risk): 37%
* Recall (low risk): 100%

<img src="images/random_forest_classifier_report.png" width="50%" height="30%">

### Easy Ensemble Classifying
* Accuracy score: 93%
* Precision (High risk): 9%
* Precision (Low risk): 100%
* Recall (High risk): 92%
* Recall (low risk): 94%

<img src="images/easy_ensemble_classifier_report.png" width="50%" height="30%">

The first step is to evaluate accuracy, looking for results as close to 1 as possible (100%). Accuracy scores help narrow down our analysis by eliminating those observations that are returning too many false returns. In the case of the credit risk analysis, the percent of high and low risk observations are identified and are actually true. The next step is to look at precision, and determine how precise predicted high and low risk evaluates to actual results. The final step is to examine recall (sensitivity), which attempts to balance high and low risk predictors. Models below listed by accuracy in descending order (A), with precision (P) and recall (R) following:

### Breakdown by Accuracy, Precision and Recall
* Easy Ensemble Classifying - A: 93%; P: high= 9%; low= 100%; R: high= 92%; low= 94%
* Balanced Random Forest Classifying - A: 68%; P: high= 88%; low= 100%; R: high= 37%; low= 100%
* SMOTEEN Sampling - A: 67%; P: high= 1%; low= 100%; R: high= 77%; low= 57%
* Random Oversampling - A: 66%; P: high= 1%; low= 100%; R: high= 69%; low= 40%
* SMOTE oversampling - A: 66%; P: high= 1%; low= 100%; R: high= 72%; low= 60%
* Cluster Centroid undersampling - A: 54%; P: high= 1%; low= 100%; R: high= 69%; low= 40%

## Summary
The precision results show an anomaly, and I was unable to determine if it was an error in my code or an accurate result. When running the balance random forest analysis, precision for high credit risk predicted was consistently 88%. Precision is calculated as the total true predicted high risk divided by the total true predicted plus the total false predicted. The confusion matrix for this model was:

| Risk Level | Predicted High Risk | Predicted Low Risk |
|------------|---------------------|--------------------|
| High       |       37            |        64          |
| Low        |        5            |     17099          |

Since there are significant numbers of actual high risk predicted to be low risk (64 in confusion matrix), I elected to exclude this model from a valid credit risk predictor in my final analysis until a team member can evaluate my code for accuracy.

Evaluating the remaining models, Easy Ensemble has a high accuracy rate (93%), while all other accuracy scores were below 70%, which I felt to be too low when attempting to predict credit risk. Easy ensemble precision rates were within acceptable parameters if slightly higher than I would prefer for high risk prediction (9%), while all other precision results were the same (1% high risk, 100% low risk). Recall rates for Easy ensesmble model were well balanced and close to 1 (high risk = 92%; low risk = 94%), while all other models had a variance between high and low I considered to be too broad for an effective credit risk prediction model.

Based on the above analysis, the Easy Ensemble model ticks all the parameters for a good prediction of credit risk.



