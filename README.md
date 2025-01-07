# Predict Which Passengers survived the shipwreck
## Overview
Predict the survival outcomes of passengers aboard the ill-fated RMS titanic.
## Problem statement
Build a predictive model that can accurately determine which passengers survived the shipwreck based on a set of features, such as age,gender, class and other personal attributes.

### Data Analysis
This project uses descriptive analysis by checking distribution of features such as age,Fare ,sex and class columns. 
The data was cleaned by filling missing numeric data with median and dropping NA that were few and had no impact to the data eg emabarked which only had 2 missing values.
I aslo dropped the Cabin column which had 77 % missing data .

One hot encoding was done for categoical values and also standardizing data before modelling
### Results
Since this is a binary classification , I used logistic regression , Decision Tree and Random Forest for modelling.
I used ROC_AUC, accuracy and MSE as evaluation metrics.
Below are the values i got

`logistic regression`

- mse_train: 0.22347266881028938
- mse_test: 0.22846441947565543
- r_Squared_train: 0.7765273311897106
- r_Squared_test: 0.7715355805243446
- roc_auc: 0.852185628742515

- Accuracy: 0.77
- Precision: 0.67
- Recall: 0.76

`decision tree`

- mse_train: 0.012861736334405145
- mse_test: 0.22846441947565543
- r_Squared_train: 0.9871382636655949
- r_Squared_test: 0.7715355805243446
- roc_auc: 0.8523652694610778

- Accuracy: 0.77
- Precision: 0.69
- Recall: 0.72

`random forest`

- mse_train: 0.012861736334405145
- mse_test: 0.22846441947565543
- r_Squared_train: 0.9871382636655949
- r_Squared_test: 0.7715355805243446
- roc_auc: 0.8523652694610778

- Accuracy: 0.77
- Precision: 0.69
- Recall: 0.72

On model evaluation the best performng model is logistic regression which generalizes well on unseen data as well. decison tree and Random Forest indicate overfitting

On hyperparameter tuning using grid search Cv for the 3 models .I settled for logistic regression with the following parameters
`Best Parameters: {'C': 0.01, 'penalty': 'l2', 'solver': 'saga'}`

### Repository Structure
```
├── data
├── submission.csv
├── titanic_survival.ipynb
├── README.md
```

