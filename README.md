# Credit_Risk_Analysis
## Objective
The objective of this project was to evaluate the performance of multiple machine learning data models and their ability to predict credit risk based upon a real-world dataset of credit card credit. The evaluations of these data models will be compared to see if any are reasonable tools to help predict credit risk. This challenge utilized Python via Jupyter Notebook, as well as utilizing scikit-learn and imbalanced-learn libraries.
<br><br>
#### Predictive Models
---
The following machine learning models were utilized in this challenge:
- **RandomOversampler** and **SMOTE** oversampling algorithms
- **ClusterCentroids** undersampling algorithm
- **SMOTEENN** combination sampling algorithm
- **BalancedRandomForestClassifier** and **EasyEnsembleAdaBoostClassifier** ensemble classifier algorithms

## Results
**RandomOverSampler Model**<br>
<kbd>![RandomOverSampler](Resources/RandomOversampler.png)<kbd>
- The balanced accuracy score of the RandomOverSampler model was 63.67%
- The precision of the high_risk credit scores was 1% and the high-risk recall was 62%, leading to a F1 score of 2%.
- The precision of the low_risk credit scores was 100% and the low-risk recall was 65%, leading to a F1 score of 79%.<br><br>

**SMOTE Model**<br>
<kbd>![SMOTE](Resources/SMOTE.png)<kbd>
- The balanced accuracy score of the SMOTE model was 63.03%
- The precision of the high_risk credit scores was 1% and the high-risk recall was 62%, leading to a F1 score of 2%.
- The precision of the low_risk credit scores was 100% and the low-risk recall was 64%, leading to a F1 score of 78%.<br><br>
 
**ClusterCentroids Undersampling Model**<br>
<kbd>![ClusterCentroids](Resources/ClusterCentroids.png)<kbd>
- The balanced accuracy score of the ClusterCentroids model was 51.04%
- The precision of the high_risk credit scores was 1% and the high-risk recall was 59%, leading to a F1 score of 1%.
- The precision of the low_risk credit scores was 100% and the low-risk recall was 43%, leading to a F1 score of 60%.<br><br>

**SMOTEENN Combination Sampling Model**<br>
<kbd>![SMOTEENN](Resources/SMOTEENN.png)<kbd>
- The balanced accuracy score of the SMOTEENN model was 63.76%
- The precision of the high_risk credit scores was 1% and the high-risk recall was 70%, leading to a F1 score of 2%.
- The precision of the low_risk credit scores was 100% and the low-risk recall was 57%, leading to a F1 score of 73%.<br><br>

**BalancedRandomForestClassifier Model**<br>
<kbd>![BalancedRandomForestClassifier](Resources/RandomOversampler.png)<kbd>
- The balanced accuracy score of the BalancedRandomForestClassifier model was 78.78%
- The precision of the high_risk credit scores was 4% and the high-risk recall was 67%, leading to a F1 score of 7%.
- The precision of the low_risk credit scores was 100% and the low-risk recall was 91%, leading to a F1 score of 95%.<br><br>
 
**EasyEnsembleAdaBoostClassifier Model**<br>
<kbd>![EasyEnsembleAdaBoostClassifier](Resources/EasyEnsembleClassifier.png)<kbd>
- The balanced accuracy score of the EasyEnsembleAdaBoostClassifier model was 92.54%
- The precision of the high_risk credit scores was 7% and the high-risk recall was 91%, leading to a F1 score of 14%.
- The precision of the low_risk credit scores was 100% and the low-risk recall was 94%, leading to a F1 score of 97%.<br><br>
 

## Conclusions
It appears that all six models exhibit very weak precision in identifying individuals who present a high credit risk. Because the vast majority of the individuals in this dataset are deemed low risk, it is unsurprising to see very high precision (rounding to 100% in all cases) given the very small possibility of a false negative. While each of the models has shown to provide weak predictive power of precision, it should be noted that the ensemble classifier algorithms provide a high recall. This indicates that they are very good at identifying high credit risk (in the case of the EasyEnsembleClassifier the recall was 91%), but also falsely identifies many low risk individuals as high risk. These false negatives exhibit a loss of potential earnings as they may go elsewhere for lower credit rates that befit their overall risk profile.<br><br>In conclusion, I would not recommend any of the six models to be used for predicting credit risk as consumer banking is a highly competitive and elastic market where overly-conservative lending will present a loss in revenue from potential credit applicants. The work performed to identify the key drivers of credit risk in the BalancedRandomForestClassifier model should be investigated further to develop a simpler model only utilizing the most important features. This would provide a more robust model with simplified input variables that would eliminate random noise introduced by non-significant variables.
