**Project Name**

Credit Card Clients (CCC) Default Prediction Using various Machine learning Algorithms

**Data Origin**

This project based on a dataset by I-Cheng Yeh (2019), Department of Information Management, Chung Hua University, Taiwan on a UCI Machine Learning Repository
https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients
description of the data and the variables values can be found in the UCI data page with the attached link.

**Analysis Description**

**note:** before the start download the data from the attached link then rename and change it's type to 'default-1.csv' then upload it to the shell you work with

Step 1 – simple data exploration using means of all the variables by defaulted person against not defaulted. also a correlation matrix between all the variables to find variables with strong correlation that can be reduced. And a linear regression to explore how strong is the correlation of independent variables (features) to the dependent variable (default).

Step 2 – fitting 7 different Machine learning algorithms with the train data:
1.	Logistic Regression (LR)
2.	Multi-layer Perceptron classifier (MLPC)
3.	Gaussian naive Bayes (GaussianNB)
4.	Suport Vector Machine (SVM)
5.	AdaBoost Classifier (Adaboost)
6.	Random Forest Classifier (RFC)
7.	K Nearest Neighbor (KNN) this algorithm was fitted 5 times with k ranging from 1 to 5.

Step 3 – test which model most accurately predict the test data

Step 4 – from step 3 I chose the 3 most accurate classifying algorithms. Using these 3 algorithms I tried to fit models but with data that was over sampled using SMOTE - Synthetic Minority Over-Sampling Technique. 

Step 5 – test the prediction accuracy of the fitted models from step 4 and compare them to the result from step 3, before the resample. The goal of steps 4-5 is to examine if the oversampling of the data contributes to our ability accurately predict the outcome, i.e credit card clients default.

Step 6 – from step 5 I choose the most accurate algorithm then Test different hyper parameters for this algorithm using a cross-validated grid-search over a parameter grid ('GridSearchCV' algorithm of scikit-learn package), to find the parameters that can give a better predictive result than the default hyper parameters used in previous steps.

**Discussion**

the best model (from the tested) that predict credit card default is Random Forest Classifier (RFC). the over sampling technique Using SMOTE improved the prediction accuracy. last point is that changing the hyper parameters from the default contribute almost nothing to the prediction accuracy.
