# M5-Walmart-Sales-Forecasting
This is Kaggle Competition for predicting next 28 data sales for products in 3 states od United States (California, Texas, and Wisconsin)

This Competition consist of sales data of 10 stores each having 30490 products from year 2011-01-29 to 22-05-2016.Out of this last 28 days are used as test data for Public Score Evaluation and next 28 days after them 23-05-2016 to 19-06-2016 are used for Private Score Evaluation in this Competition.<br/>In this Competition are using Weighted Root Mean Squared Scaled Error(WRMSSE) as evaluation metric. There are some Traditional Statistical Approcahes Like ARIMA,ARIMAX etc. But Here We Will Try various Machine Learning Models For Predicting 28 days sales.



They have given Several Files like:-
<br/>calendar.csv - Contains information about the dates on which the products are sold.
<br/>sales_train_validation.csv - Contains the historical daily unit sales data per product and store [d_1 - d_1913]
<br/>sell_prices.csv - Contains information about the price of the products sold per store and date.
<br/>sales_train_evaluation.csv - Includes sales [d_1 - d_1941] (labels used for the Public leaderboard)

More information on:https://www.kaggle.com/c/m5-forecasting-accuracy/overview  or the Notebooks given in Notebooks Folder in this repository
 In this Repository there are following notebooks:-
 <br/>1. EDA.ipynb :- This Notebook describes all Exploratory data Analysis done on data and preperation/combining of data provided in kaggle for futher processing.In this we have given several plot to see how sales are varying according to state,category,department etc.
 <br/>2. FeatureEngineering.ipynb :- This Notebook describe all Feature Engineering we have done on the data.We have varoius time series and date related done feature engineering in this notebook.
 <br/>3. Modeling.ipynb :- This Notebook contain various Models  used for sales forecasting ,Here We have Shown result by both custom implementation of WRMSSE on test and cv data and Public and Private score on kaggle.
 
Features<br/>1. item id<br/>
2. store_id<br/>
3. cat_id <br/>
4. department<br/>
5. state_id<br/>
6. month<br/>
7. year<br/>
8. snap (i.e. is today a snap day for the current store)<br/>
9. weekday<br/>
10. Date Related Features (month end/start,year end/start,quater end/start,week number)<br/>
11. Time Series Related Features (Lag Features,Rolling average,Exponential Weighted Average all with shift more than 28 days to avoid data leakage)  <br/>

Models Used<br/>1. Linear Regression
<br/>2. LSTM Neural Network
<br/>3. CNN-LSTM Neural Network
<br/>4. Light GBM Model
<br/>5. AdaBoost Regressor Model
<br/>6. CatBoost Model

Special Thanks to Konstantin Yakovlev kernels in kaggle from where I have got to learn many things in this competition(Especially combing all 3 snaps as one).<br/>
References:-<br/>1.https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/163684<br/>2.https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/164374 <br/>3.https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/163578<br/>4.https://www.kaggle.com/kyakovlev/m5-simple-fe<br/>4.https://www.kaggle.com/c/m5-forecasting-accuracy/discussion/164599
