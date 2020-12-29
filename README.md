# Detecting-fraud-with-ML

## Project description: 

We use a dataset from a private anonymous company in order to classify fraudulent clients taking other variables such as age, gender, browser used to shop, among 
others as explnatory variables.

## Methodologies:

After cleaning the dataset we start with a exploratory visualisation analysis of the data (univariate and multi variate). We register 9.4% of fraudulent clients on the dataset. After some feature engineering pipeline specifically built to handle the difference between the cathegorical and the numerical explanatory variables (Kbins discretizers from scikitlearn) we built a Bernoulli naive Bayes model for a split of 30% between train and test sets on the data. The Naive Bayes model performw well with a confusion matrix fully charged detecting all the classes for this unbalanced dataset. The Naive Bayes model predicts a rate of fraud of 9.36 % (the empirical rate of fraud is 9.4 %), the false negative rate is 4.11 and the false positive rate is 4.74 %. The ROC (receiving operating characteristic)for this model is 75% on the prediction of probabilities of fraud on the test set. About the hierarchy of feature importance: 
time_delta of the purchases, the country with higher fraud percentages, the source and the browser from the purchase and age are the most important variables according to the NAive Bernoulli Bayes model to understand and predict fraud probabilities. As a second approach we use support vector machines to predict fraud. This second model has a score of 0.931111307186659. We use GridSearchCV for hyper parameter tunning and we retrieve as optimal parameters {'C': 50, 'gamma': 0.005}. For these optimal parameters the score on the train set is 0.9071356992947494
againsts (a non over fitting) score on the test set of 0.9073101866149027.



## Resources and code used:

**Python version:** 3.7
**Libraries/packages used:** pandas, numpy, scikitlearn, matplotlib, seaborn
**Dataset:** available at the repo
