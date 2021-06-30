# Credit_Risk_Analysis
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


<h3 align="center"> Undersampling </h3>
<p align = "center">
 <img src="images/undersampling.png">
</p>


<h3 align="center"> Combination Sampling </h3>
<p align = "center">
 <img src="images/combo_sampling.png">
</p>


<h3 align="center"> Balanced Random Forest Classifier </h3>
<p align = "center">
 <img src="images/random_forest.png">
</p>


<h3 align="center"> Easy Ensemble AdaBoost Classifier </h3>
<p align = "center">
 <img src="images/ez_boost.png">
</p>


## Summary

