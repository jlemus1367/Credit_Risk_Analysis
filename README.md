# Credit Risk Analysis
## Project Overview
For this project, we applied various machine learning models to predict credit risk with imbalanced-learn and scikit-learn. Given a dataset with many features, we created models to classify the target variable as low-risk or high-risk applicants. We applied several models to the same dataset due to the complex nature of credit risk, specifically the unbalanced classification problem where good loans outweigh risky loans in the dataset. The class imbalance creates a situation where the models are better at predicting one class than the other.  Therefore, we applied models to handle the classification problem such as oversampling, SMOTE,  and undersampling. We then used models that help reduce bias and compared the results of all the models to determine which one was the best for predicting credit risk. 

## Resources
- Python 3.7.6
  - Pandas
  - Scikit-learn
- Jupyter Notebook

## Results

<h3 align="center"> Naive Random Oversampling </h3>
<p align = "center">
 <img src="images/oversampling.png">
</p>

- The balanced accuracy score for the Naive Random Oversampling model was 0.662
  - i.e., our model was 66.2% accurate
- The precision for high-risk loans was 1 %
  - Out of the 6,723 loans that were predicted to be high-risk, only 72 were actually high-risk
- The sensitivity for high-risk loans was 71 %
  - Out of the 101 risky loans, 72 were predicted correctly as high-risk loans
- The precision for low-risk loans was 100 %
  - Out of the 10,482 loans that were predicted to be low-risk, 10,453 were actually low-risk
- The sensitivity for low-risk loans was 61 %
  - Out of the 17,104 safe loans, 10,453 were predicted correctly as low-risk loans

<h3 align="center"> SMOTE Oversampling </h3>
<p align = "center">
 <img src="images/smote.png">
</p>

- The balanced accuracy score for the SMOTE Oversampling model was 0.663
  - i.e., our model was 66.3% accurate
- The precision for high-risk loans was 1 %
  - Out of the 5,321 loans that were predicted to be high-risk, only 64 were actually high-risk
- The sensitivity for high-risk loans was 63 %
  - Out of the 101 risky loans, 64 were predicted correctly as high-risk loans
- The precision for low-risk loans was 100 %
  - Out of the 11,884 loans that were predicted to be low-risk, 11,847 were actually low-risk
- The sensitivity for low-risk loans was 69 %
  - Out of the 17,104 safe loans, 11,847 were predicted correctly as low-risk loans


<h3 align="center"> Undersampling </h3>
<p align = "center">
 <img src="images/undersampling.png">
</p>

- The balanced accuracy score for the Undersampling model was 0.544
  - i.e., our model was 54.4 % accurate
- The precision for high-risk loans was 1 %
  - Out of the 10,410 loans that were predicted to be high-risk, only 70 were actually high-risk
- The sensitivity for high-risk loans was 69 %
  - Out of the 101 risky loans, 70 were predicted correctly as high-risk loans
- The precision for low-risk loans was 100 %
  - Out of the 6,795 loans that were predicted to be low-risk, 6,764 were actually low-risk
- The sensitivity for low-risk loans was 40 %
  - Out of the 17,104 safe loans, 6,764 were predicted correctly as low-risk loans


<h3 align="center"> Combination Sampling </h3>
<p align = "center">
 <img src="images/combo_sampling.png">
</p>

- The balanced accuracy score for the Combination Sampling model was 0.666
  - i.e., our model was 66.6 % accurate
- The precision for high-risk loans was 1 %
  - Out of the 7,106 loans that were predicted to be high-risk, only 75 were actually high-risk
- The sensitivity for high-risk loans was 74 %
  - Out of the 101 risky loans, 75 were predicted correctly as high-risk loans
- The precision for low-risk loans was 100 %
  - Out of the 10,099 loans that were predicted to be low-risk, 10,073 were actually low-risk
- The sensitivity for low-risk loans was 59 %
  - Out of the 17,104 safe loans, 10,073 were predicted correctly as low-risk loans

<h3 align="center"> Balanced Random Forest Classifier </h3>
<p align = "center">
 <img src="images/random_forest.png">
</p>

- The balanced accuracy score for the Balanced Random Forest Classifier model was 0.789
  - i.e., our model was 78.9 % accurate
- The precision for high-risk loans was 3 %
  - Out of the 2,224 loans that were predicted to be high-risk, only 71 were actually high-risk
- The sensitivity for high-risk loans was 70 %
  - Out of the 101 risky loans, 71 were predicted correctly as high-risk loans
- The precision for low-risk loans was 100 %
  - Out of the 14,981 loans that were predicted to be low-risk, 14,951 were actually low-risk
- The sensitivity for low-risk loans was 87 %
  - Out of the 17,104 safe loans, 14,951 were predicted correctly as low-risk loans


<h3 align="center"> Easy Ensemble AdaBoost Classifier </h3>
<p align = "center">
 <img src="images/ez_boost.png">
</p>

- The balanced accuracy score for the Easy Ensemble AdaBoost Classifier model was 0.932
  - i.e., our model was 93.2 % accurate
- The precision for high-risk loans was 9 %
  - Out of the 1,076 loans that were predicted to be high-risk, only 93 were actually high-risk
- The sensitivity for high-risk loans was 92 %
  - Out of the 101 risky loans, 93 were predicted correctly as high-risk loans
- The precision for low-risk loans was 100 %
  - Out of the 16,129 loans that were predicted to be low-risk, 16,121 were actually low-risk
- The sensitivity for low-risk loans was 94 %
  - Out of the 17,104 safe loans, 16,121 were predicted correctly as low-risk loans

## Summary

After running all six models, it appears that they all have very low precision for predicting high-risk loans. The models incorrectly label low-risk applicants as high risk more often than not. Both oversampling models performed similarly with an accuracy of 66 percent, and the undersampling model performed the worst with an accuracy score of 54  percent. Using a combination of oversampling and undersampling to compensate for unbalanced classes did not make much of a difference regarding the accuracy score. However, the sensitivity for accurately detecting high-risk applicants from the actual pool of high-risk applicants was slightly better. 

The random forest and ensemble boost models used to reduce bias performed strikingly better than the other models. They had accuracy scores of 78 percent and 93 percent, respectively. Their precision for detecting high-risk loans was better than all other models. The ensemble model had the best precision and sensitivity for high-risk loans. However, we must also be cautious of the potential overfitting that may have occurred with these models.

In the context of credit lending, it is more critical that we correctly pedict high-risk applicants from the pool of applicants who are actually high risk, so sensitivity is more important than precision. However, the precision for predicting high-risk loan applicants is way too low for all of our models. By wrongfully overmarking those who are low-risk as high-risk, we miss out on potential revenue. As a result, non of the models are ideal for detecting credit risk. 

