# flight price prediction
Data taken from the Kaggle.

## Importing dataset

1. Since data is in form of excel file we have to use pandas read_excel to load the data
2. After loading it is important to check the complete information of data as it can indication many of the hidden infomation such as null values in a column or a row
3. Check whether any null values are there or not. if it is present then following can be done,
    1. Imputing data using Imputation method in sklearn
    2. Filling NaN values with mean, median and mode using fillna() method
4. Describe data --> which can give statistical analysis

From description we can see that Date_of_Journey is a object data type,\
Therefore, we have to convert this datatype into timestamp so as to use this column properly for prediction

For this we require pandas to_datetime to convert object data type to datetime dtype.
.dt.day method will extract only day of that date.
.dt.month method will extract only month of that date.

## Handling Categorical Data
One can find many ways to handle categorical data. Some of them categorical data are,
1. Nominal data 
  data are not in any order, OneHotEncoder is used in this case.
2. Ordinal data
  data are in order, LabelEncoder is used in this case.

## Feature Selection
Finding out the best feature which will contribute and have good relation with target variable.
Following are some of the feature selection methods,
1. heatmap
2. feature_importance
3. SelectKBest

## Fitting model using Random Forest

1. Split dataset into train and test set in order to prediction w.r.t X_test
2. If needed do scaling of data
    * Scaling is not done in Random forest
3. Import model
4. Fit the data
5. Predict w.r.t X_test
6. In regression check **RSME** Score
7. Plot graph

## Hyperparameter Tuning


* Choose following method for hyperparameter tuning
    1. RandomizedSearchCV --> Fast
    2. GridSearchCV
* Assign hyperparameters in form of dictionery
* Fit the model
* Check best paramters and best score
