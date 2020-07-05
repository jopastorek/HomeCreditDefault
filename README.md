# Home Credit Default Prediction
![](https://assets.entrepreneur.com/content/3x2/2000/20200406144106-GettyImages-1023100020.jpeg?width=700&crop=2:1)

From the description of the [Kaggle completition](https://www.kaggle.com/c/home-credit-default-risk/overview):

  "Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders.
  Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. In order to make sure this underserved population has a positive loan experience, Home Credit makes use of a variety of alternative data--including telco and transactional information--to predict their clients' repayment abilities.
  While Home Credit is currently using various statistical and machine learning methods to make these predictions, they're challenging Kagglers to help them unlock the full potential of their data. Doing so will ensure that clients capable of repayment are not rejected and that loans are given with a principal, maturity, and repayment calendar that will empower their clients to be successful."

The goal of this project is to complete a full data science lifecycle including the following topics:

1. Business Understanding
Following the Kaggle evaluation the ROCAUC between the predicted probability and the observed target is used.

2. Data Mining

The Kaggle competition consists of eight data sets of which only one is used here (application_{train|test}.csv). This is the main table, broken into two files for Train (with TARGET) and Test (without TARGET). Static data for all applications. One row represents one loan in our data sample.
No further data mining will be carried out here.
3. Data Cleaning

Around 24 % of all the data points are missing, hence a main task is to decide how to approach this problem. Some date type features have negative days as unit which is transformed to number of years (division by -365). Outliers and 'XNA' values are replaced with NaN values. Imputed will be done as follows: NaN's in categorical features will be replaced with 'missing', NaN's in numerical features will be replaced with the median value of the respective feature's value of the TRAIN data set. For XGBoost only categorical imputation will be carried out.
4. Data Exploration

5. Feature Engineering

6. Predictive Modeling

7. Data Visualization
