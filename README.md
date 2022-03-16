# Appliances Energy Prediction - Supervised ML Regression Capstone Project

## Problem Statement- 
Main purpose of this project is to predict appliance energy consumption using linear regression algorithms.
## Summary- 
We got a dataset having around 20000 records and 29 features. In our dataset we have 28 independent variables and 1 dependent labelled feature. So I performed EDA on data to get some insights from it, then I checked for missing/duplicate values, after that I checked for outliers. After these data cleaning process I performed data visualization to know insights from our data. After visualization I checked correlation between variables and then moved towards feature engineering. After feature engineering I decided to build regression models on it. First I built linear regression model and after that I built random forest regressor model, and evaluated both the models. In which random forest was the best performer.

## Components & Approach-
## 1. Exploratory Data Analysis

### a. Understanding the data- 
In this step after loading the data I performed head, tail, columns, info, dtypes, describe functions to get basic information about our dataset.
### b. Checking for missing & duplicated values- 
Then I checked for missing values in our dataset using is null function, but we don’t have a single missing value. After that checked for duplicated values using duplicated function.
### c. Cleaning Dataset- 
As we don’t have any missing or duplicated value we don’t need to do with that. But I renamed some of the columns for better understanding while performing further operations.
### d. Outlier Detection- 
I selected top 0.1% of records from target variable as outlier and removed them.

## 2. Data Visualization – 
In data visualization I got insights from various features. From 7 AM to 11
AM there is clear spike in energy consumption (from 80 wh to 135 wh), because in morning
session we use lot of appliances for various purpose. From 4 pm to 6 pm we can spot a sudden
hike (from 120 wh to 185 wh) in energy consumption following by a sudden fall from 185 wh to
70 wh during 6 PM to 10 pm in night.
The power load is a bit higher on Monday, Friday, Saturday and Sunday than the other days.
In February, Monday and Thursday having high consumptions. March has Monday and Saturday
as high energy consumers with Tuesday as low consumer. In April, Friday has more energy
consumption and Thursday has the least. In May Fridays and Saturdays have highest consumption
where Tuesdays has least consumption. Features that have high correlation with dependent
variable (log_appliances) are hour, t_out, lights, t6, rh_6, t2, t3, rh_out, rh_8, wind speed.

## 3. Feature Engineering- 
After data visualization I performed feature engineering for linear
regression using correlation heat map and pair plot. After feature selection I converted all
categorical features into numerical using get dummy. For Random forest regressor first I fitted
model on data with all features, and then calculated feature importance score for all features and
selected features with high score.

## 4. Data Pre-processing-
### Train-Test Split
Splits the data into 80:20 ratio for training and testing purpose respectively, using ‘sklearn’ train
test split metrics.

## 5. Model Building-
### a. Linear Regression- 
Linear Regression is a machine learning algorithm based on supervised learning. It performs a regression task. Regression models a target prediction value based on
independent variables. It is mostly used for finding out the relationship between variables and
forecasting.
### b. Random Forest Regressor- 
A random forest is a Meta estimator that fits a number of
classifying decision trees on various sub-samples of the dataset and uses averaging to improve
the predictive accuracy and control over-fitting.

## 6. Evaluating Models –
After evaluating both the model I got R2 score for linear regression as 37% and for Random forest
I got 64%, so it was clear that random forest regressor is best model.

## 7. Hyperparameter Tuning-
For hyper-parameter tuning I used Grid Search CV, and after tuning I evaluated random forest
regressor model again but this time I got slightly low r2 score so I decided to go with my first
model.

## 8. Conclusion-
a. The power load is a bit higher on Monday, Friday, Saturday and Sunday than the other days.
b. On daily basis, from 7 AM to 11 AM there is clear spike in energy consumption (from 80 wh to
135 wh), because in morning session we use lot of appliances for various purpose.
c. From 4 pm to 6 pm there is a sudden hike (from 120 wh to 185 wh) in energy consumption
following by a sudden fall from 185 wh to 70 wh during 6 PM to 10 pm in night.
d. In linear regression model our R2 score is around 37% which means our model is capturing only
37% variance. We can say it’s not having enough R2 score.
e. In random forest regressor our R2 score is around 0.639 which means our model is predicting 64%
accurately. And it is much accurate than linear regression model.

# Thank You....!
