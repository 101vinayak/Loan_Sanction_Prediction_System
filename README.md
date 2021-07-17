# Loan_Sanction_Prediction_System
A ML based Loan amount sanction prediction model to predict the amount that can be sanctioned to the person based on various features.
The code resulted in an 87 score on CIPLA Hiring test for Data Scientist role on D2C.

The Following steps were used to reach the score:
1. The Data was analysed for categorical and continuous valued features and deal with them seperately.
2. The categorical features were Label Encoded.
3. Firstly, the missing values were handled, columns with large amount of missing values were droppped, after analysing their correlation factors.
4. The rest missing values were replaced with mode/mean/etc as per the values of the feature.
5. Finally a correlation matric was built to check for various feature relationships, features with very high(>85%) correlation were dropped, and columns with very    low(<15%) correlation to the "Loan Sanction Amount" feature were dropped as they did not contribute to the prediction much.
6. A few columns were important but had considerable missing values, for them a Linear Regression model was built based on other features, and the missing values      were predicted, based on their relation with other features.
7. Finally this dataset was saved and an XGBoost Regressor model was used to predict the "Loan SAnction amount" of the test dataset after being trained.

The following are the first 100 value comparisons of the predicted and actual amount.\
![alt text]()
