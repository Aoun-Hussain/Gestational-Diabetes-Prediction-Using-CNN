
# [SweetExpectations](https://sweet-expectations.herokuapp.com/) 
[![GitHub forks](https://img.shields.io/github/forks/Harmeet2504/Insight_Health?style=for-the-badge)](https://github.com/Harmeet2504/Insight_Health/network)
[![GitHub stars](https://img.shields.io/github/stars/Harmeet2504/Insight_Health?style=for-the-badge)](https://github.com/Harmeet2504/Insight_Health/network)
[![GitHub license](https://img.shields.io/github/license/Harmeet2504/Insight_Health?color=red&style=for-the-badge)](https://github.com/Harmeet2504/Insight_Health/network)

### Predicting gestational dibetes for timely intervention 
An end-to-end data modeling project as a postdoctoral fellow at Insight

## Content
1. [Summary](#Summary)
1. [Packages](#Packages)
1. [Data](#Data)
1. [EDA](#EDA)
1. [Features](#Features)
1. [Training](#Training)
1. [Validation](#Validation)
1. [App](#App)
1. [Challenges](#Challenges)
1. [Installations](#Installations)
1. [How-to-run](#How-to-run)
1. [Presentation](#Presentation)

## Summary
The aim of this project is to build a web application to predict/monitor the risk of gestational diabetes in expectant women much before their Oral Glucose Tolerance Test is due(around week 26-28).Early prediction promotes timely lifestyle interventions which essentially translates to an estimated saving of $5800 per pregnancy per an estimate by The American Diabetes Association.

## Packages
Python, pandas, matplotlib, seaborn, numPy, sklearn, HTML, CSS, Flask, Bootstrap, Heroku

## Data
Electronic Health Records of expecting women were pulled in from [Physionet](https://www.physionet.org/content/maternal-visceral-adipose/1.0.0/).The database is from a cohort study of pregnant women up to 20 weeks of pregnancy and followed until delivery.Total records is 133. Inclusion criteria were singleton pregnancy and gestational age ≤20 weeks.
        ![Pipeline](https://github.com/Harmeet2504/Insight_Health/blob/master/reports/figures/pipeline.jpg)
## EDA
Data was cleaned using pandas, and explored using matplotlib, seaborn visualization libraries. The data has 13 features and 1 target (gestational diabetes mellitus (gdm)), with imbalanced class (14% positive and 86% negative). Positive cases have a mean age of 29 years, tend to be obese with high first fasting blood glucose. 

## Features
Features that did not meet inclusion criteria (type of delivery, gestational age at delivery, child birth weight at delivery) and had no signal (previous diabetes) were dropped.  Recursive feature elimination with cross-validation suggested 8 features for optimum accuracy, 'Ethnicity' being the weekest. Furthermore, redundancy was taken care of by exclusion of highly correlated features (mean diastolic bp, mean systolic bp, armenalli fat (pearson coefficient of correlation > 0.50)) without impacting the overall model performance. Final feature vector was composed of 5 features (Fasting blood glucose (mg/dl), BMI Pregestational, Age, Pregnancies (number), Gestational age).

## Training
Data was stratified before splitting to training(80%) and test(20%) set using sklearn. Resampling was implemented on the training set to match the minority with majority class. Random forest classifier was formulated and tuned for its hyperparameters using 3-fold cross-validation by leveraging randomized search algorithm.

## Validation
Model was optimized to eliminate false negative and precisely identify true outcomes because in either case any interventions would affect the life of both mother and the child. Hence, evaluation criteria was a trade-off of sensitivity/recall and precision. Model had an F1-score of 95% (used because unequal class distribution), Recall/Sensitivity of 100%, Precision of 93%. All the parameters were better than the baseline model by 25% with an offset of 3% for Specificity.
                                
                    
  ![Validation](https://github.com/Harmeet2504/Insight_Health/blob/master/reports/figures/evaluation_comparison.png)
                    
                    

## App
The app was built using Flask api, designed with HTML, CSS and Bootstrap and deployed on Heroku. 

## Challenges
1. Small sample size: Feature space was reduced to build a generalizable model.Random Forest Classifier is a robust algorithm that works on the principle of bagging and eliminates overfitting by lowering variance.
2. Imbalanced classes: Balancing class-weights didn't fetch good result due to small size. The best way around was to randomly oversample the minority class to match majority class in the training set.

## Installations
pip install -r requirements.txt

## How-to-run 
1. Clone the repository 
2. Set up the environment variables
3. run 'python app.py' from root directory

## [Presentation](https://docs.google.com/presentation/d/1tOQLsVaOKyczOl9bWyY8tBFNd4tDgh6xUF0ByhJN0Rg/edit?usp=sharing)
