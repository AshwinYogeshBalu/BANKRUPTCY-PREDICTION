# BANKRUPTCY-PREDICTION

## Problem Statement
##### Bankruptcy is known as a status where a firm cannot repay any of the debts. There are a lot of creditors/investors who wish to invest in the growing companies. But, it is important to understand the financial stability of the company before investing on them. In other words, it is important to identify whether a company will go bankrupt or not before investing on the firm. The usecase of this project is concerned about the investors who are planning on investing in the polish companies. Our assumption is that, the investors wants to be so sure about the financial stability of a company before investing on them. In other words, the investors must be able to identify and be cautious about the companies that are at the verge of bankruptcy.

## Data Source
##### The data was collected from Emerging Markets Information Service which is a database containing information on emerging markets around the world. The bankrupt companies were analyzed in the period 2000-2012, while the still operating companies were evaluated from 2007 to 2013. Basing on the collected data five classification cases were distinguished. Each of the classification corresponds to one forecasting period. Hence, we have 5 sets of records which we will be combining into a single file.

## Data Description
##### It has 64 predictor variables which are all numerical. It has a binary target variable which indicates the bankruptcy. There are 43405 records for a total fo 5 years. The target variable is imbalanced. The success class 1 accounts for only 4.82 % of the entire dataset.

## Data Mining Tasks
##### Data summary exploration, Missing data exploration, Correlative analysis, Class imbalance analysis

## Data Mining Models
##### Logistic Regression - with SMOTE & without SMOTE, Soft Margin SVM

## Performance Evaluation
### 1) Logistic Regression - without SMOTE
##### The accuracy of the model is so good. We got a 95% accuracy. But the usecase of this project is more concerned about identifying the success class 1 correctly. In that case, recall is what matters to us. Our model has performed so bad in terms of identifying the minority success class. We achieved a recall of only .007.

### 2) Logistic Regression - with SMOTE
##### After oversampling the data, we have given enough data points of the minority class to the model. The recall should improve after training the model on the over-sampled data. This is our assumption. Our assumption is true. The recall has significantly improved to 0.65. This has occurred by having trade-off with accuracy. But the f1 score is still low.

### 3) Soft Margin SVM
##### The f1 score of SVM model has increased to 0.27 compared to the f1 score of the previous model. But the model has still failed to perform well. This is because, the value of recall has gone down compared to the previous model.

## Conclusion
##### We chose logistic regression as our baseline model. The model performed bad initially as there was class imbalance in the data. After doing oversampling, the model performed good and gave a better recall value. But, it was not a great model as the f1 score was low. To increase the f1 score without sacrificing the recall value, SVM model was chosen as it is a non- linear classifier. We assumed SVM to perform well and give better results, both in terms of recall and f1 score. But, the model didn’t perform well as expected. As a next step, neural networks could be implemented on the data as neural networks perform well with higher dimension data.
