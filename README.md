# Credit Risk Analysis

## Overview
This credit risk analysis examines data from LendingClub, a peer-to-peer lending service company. Credit risk is an unbalanced classification problem, because good loans easily outnumber risky loans. Therefore, the research department has been tasked with employing different machine learning techniques to train and evaluate models using resaampling.

This analysis will use the LoanStats_2019Q1.csv dataset, imbalanced-learn and scikit-learn libraries to perform the analysis. The following models will be used for the analysis:
    Naive Random Oversampling
    SMOTE Oversampling
    Cluster Centroid Undersampling
    SMOTEENN Sampling
    Balanced Random Forest Classifying
    Easy Ensemble Classifying

## Results
Bulleted list describes balanced accuracy score and the precision and recall scores of all six machine learning models.

### Naive Random OverSampling
* Accuracy score: 66%
* Precision (High risk): 1%
* Precision (Low risk): 100%
* Recall (High risk): 72%
* Recall (low risk): 60%

<img src="images/random_oversampling_report.png" width="40%" height="20%">

### SMOTE Oversampling
* Accuracy score: 66%
* Precision (High risk): 1%
* Precision (Low risk): 100%
* Recall (High risk): 62%
* Recall (low risk): 69%

<img src="images/smote_oversampling_report.png" width="40%" height="20%">

### ClusterCentroid Undersampling
* Accuracy score: 54%
* Precision (High risk): 1%
* Precision (Low risk): 100%
* Recall (High risk): 69%
* Recall (low risk): 40%

<img src="images/clustercentroid_undersampling_report.png" width="40%" height="20%">

### SMOTEEN Sampling
* Accuracy score: 67%
* Precision (High risk): 1%
* Precision (Low risk): 100%
* Recall (High risk): 77%
* Recall (low risk): 57%

<img src="images/smoteen_report.png" width="40%" height="20%">

### Balanced Random Forest Classifying
* Accuracy score: 68%
* Precision (High risk): 88%
* Precision (Low risk): 100%
* Recall (High risk): 37%
* Recall (low risk): 100%

<img src="images/random_forest_classifier_report.png" width="40%" height="20%">

### Easy Ensemble Classifying
* Accuracy score: 93%
* Precision (High risk): 9%
* Precision (Low risk): 100%
* Recall (High risk): 92%
* Recall (low risk): 94%

<img src="images/easy_ensemble_classifier_report.png" width="40%" height="20%">

## Summary
Summarized results
recommendation on which model to use, or no recommendation with justification.
