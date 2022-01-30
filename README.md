# Bankruptcy_Prediction
Classification of Company Bankrupty

[Open My Notebook - Bankruptcy Classification](https://colab.research.google.com/drive/1Ebst3JfQvHyLS7MHsJuH33o4dz5islVy?usp=sharing)

# Overview
This repository features EDA and classification on the [Company Bankruptcy Prediction](https://www.kaggle.com/fedesoriano/company-bankruptcy-prediction) kaggle data set.

# Bankruptcy Distribution
The mean bankruptcy rate of this data set is 3.15%.

# Missing Data and Outliers
There is no missing data.

There are a lot of outliers in this data. There are 6 columns with 1,000 + outliers. These outliers were not changed. Columns with a high number of outliers were examined and some outliers seemed related to bankruptcy.

# Data Preparation for Modeling

All data was numeric, and standardized prior to modeling.

# Modeling - Logistric Regression, Naive Bayes, and SVM.

Logistic regression had the best performance, with an f1 score of .356. The naive bayes model had an f1 score of .1645, and the SVM model had a f1 score of .1356.

The SVM model was tuned to use an rbf kernel with a c of 100 and gamma of .0001.

# Logisitc Regression Model Assumptions

Binary logistic regression requires a binary response variable, observations to be independant of one another, little multicollinearity, linearity of independent variables and log odds, and a large sample size.

With 6,819 records, there is a relatively large sample size but I am using all 95 variables in my models. With a mean default of 3.15%, and 95 predictor variables, the ideal general sample size would be around 30,000.

There is collinearity among independant variables, with some correlations greater than .80. Reducing features for future models will promote sample size and multicollinearity assumptions are met.
