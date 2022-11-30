# Churn-Prediction

## Dependencies:
- PyCaret
- - Used for Model Selection
- - Installation: pip install pycaret

- Boruta
- - Used for *selecting important features*
- - Installation: pip install boruta

- Optuna
- - Used for Hyper parameter tuning
- - Installation: pip install optuna

- CatBoost
- - Used the CatBoost Classifier for predicting *Churn*
- - Installation: pip install catboost

- XGBoost
- - Used the XGBoost Classifier for predicting *Churn*
- - Installation: pip install xgboost

- LightGBM
- - Used the LightGBM Classifier for predicting *Churn*
- - Installation: pip install lightgbm

- SciKit Learn

- Pandas

- Numpy


## Importing data 
- Imported the data provided in the zip file


## Ensuring proper *data types*
- The *Target Charges* column is supposed to have a *data type* of *float* but was instead initialized as *object* as there were missing values in the form of empty spaces
- Changed the data type to float and filled the missing values with median imputation


## Encoding Categorical Features
- Encoded *binary* columns to 0s and 1s
- Encoded *ordinal features* as 0s , 1s and created a new features from the remaining
- *One Hot Encoded* the Nominal features


## Scaling the data and Splitting 
- Scaled the data with *Robust Scaler* as there were huge outliers
- Then used *min max scalar* to scale the results 
- Split the data into *Train* and *Test*


## Feature Selection 
- Feature selection using Chi2
- Feature importance using coefficients of *Logistic Regression Classifier*

![](https://github.com/AnandBallure/Razorpay-Churn-Prediction/blob/main/Feature%20Importance%20logReg.png)

- Implemented *Boruta* for selecting the important features
- Prioritized the top 6 features


## Model Selection 
- Implemented *PyCaret* for selecting the models
- Selected 6 top performing models


## Hyper-parameter Tuning
- Implemented *Optuna* for tuning the hyper-parameters of various models while monitoring the accuracy


## Bagging the Models and Training
- Bagged the models for better prediction accuracy by using *Voting Classifier*
- Trained the model


## Results and Evaluation
- Made predictions on the test data 
- Evaluated using *accuracy*
- Avchieved an accuracy of 80.09%
- Confusion Matrix:
![](https://github.com/AnandBallure/Razorpay-Churn-Prediction/blob/main/Churn.png)
- Classification Report:
![](https://github.com/AnandBallure/Razorpay-Churn-Prediction/blob/main/Classification%20Report.png)
