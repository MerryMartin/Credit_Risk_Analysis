# Credit_Risk_Analysis

## Project Overview
### Purpose
For this project, I needed to evaluate a credit card dataset in order to analyze and predict future high risk loans.  Since low risk loans greatly outnumber high risk loans and the classes in the dataset are unbalanced, it can be difficult to correctly assess the loan risk.  
### Process
To address the issue of imbalanced classes in the datatset, I prepared the data and then built and avaulated machine learning models with RandomOverSampler, SMOTE oversampling, ClusterCentroids undersampling and SMOTEEN combination sampling.  I then compared two ensemble algorithms, BalancedRandomForestClassifier and EasyEnsembleClassifier, to try and minimize bias.  Finally, I compared the results for all the models so I could eventaully recommend a good approach for predicting credit risk.   

## Results
### Algorithm Analysis
All models were evaluated by calculating their accuracy score, generating a confusion matrix, and printing out the imbalanced classification report.

* Naive Random Oversampling Results:
    * Balanced Accuracy:  65%
    * Precision (high_risk):  1%  
    * Recall (high_risk):  72%
    
![RandomOverSampler](https://user-images.githubusercontent.com/115426070/219732377-7e050985-deea-4cd1-ba90-74e657c3c6a4.png)




* SMOTE Oversampling Results:
    * Balanced Accuracy:  66%
    * Precision (high_risk):  1%  
    * Recall (high_risk):  63%

![SMOTE](https://user-images.githubusercontent.com/115426070/219732450-18696698-0f74-4814-845b-fdc5a9700383.png)



* Cluster Centroids Undersampling Results:
    * Balanced Accuracy:  54%
    * Precision (high_risk):  1%
    * Recall (high_risk):  69%

![ClusterCentroids](https://user-images.githubusercontent.com/115426070/219732522-32d653e3-7977-40c3-bba4-dd0b115cdeed.png)



* SMOTEEN Combination Sampling Results:
    * Balanced Accuracy:  6%4
    * Precision (high_risk):  1% 
    * Recall (high_risk):  71%

![SMOTEEN](https://user-images.githubusercontent.com/115426070/219732590-bfcf8e3b-0bce-4c13-8dc8-741f68ef431e.png)



* Balanced Random Forest Classifier Results:
    * Balanced Accuracy:  87%
    * Precision (high_risk):  3% 
    * Recall (high_risk):  70%

![BalancedRandomForestClassifier](https://user-images.githubusercontent.com/115426070/219732655-02f30425-e595-4b72-a113-0f6d38c2a59d.png)



* Easy Ensemble Classifier Results:
    * Balanced Accuracy:  94%
    * Precision (high_risk):  9% 
    * Recall (high_risk):  92%

![EasyEnsembleClassifier](https://user-images.githubusercontent.com/115426070/219732700-9b33d2dc-dd25-4cbb-a99b-26970fa5cd08.png)




## Summary
### Feature Importance
According to the analysis, the following features are the most important, when detecting high_risk loans
![Top_Five](https://user-images.githubusercontent.com/115426070/219732750-43711432-35b7-4820-bcc1-4a2aeca887ef.png)



### Model Evaluation
The Easy Ensemble Classifier had the best results for detecting high risk loans of all the models, with an accuracy rate of 94% and a precision of 9%.   However, 9% is a relatively low precision and means that there are likely to be more actual positives (high risk loans) that are missed by this model. Also, the model has a high sensitivity (recall) of 92% which means that it does a good job detecting the high_risk loans but might also result in a lot of false positives.  Since we want to limit the lendors exposure to high_risk loans but don't want to unneccesarily penalize applicants that might not actually be in the high_risk class, we need to have a balance of precision and sensitivity.  None of the models evaluated have a good balance and so I would not reccomend using them to detect high risk loans.   




 
