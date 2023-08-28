# HILPISCH_wget
ALGO_TRADING_HILPISCH_wget

HILPISCH - ALGO Trading Project on Oil price moves

Author: Raphael Bruggmann

Date: 30.08.2023

Location: Zuerich

The aim of this project is to develop an algorithmic trading notebook that models different types of strategies using any applicable market instrument from tqoa-Oanda/Reuters. As we cannot integrate the API directly, we will use static data in this project. Our strategy will be focused on the "BRENT" instrument Cal 2005 to Cal 2023.
To forecast the market's direction (up or down), we will use a broad library of model approaches. The range of models integrated into the project is intentionally wide, spanning from very static conventional approaches to more machine learning approaches. It is important that all the chosen models in the project remain comparable based on their cumulative returns, the accuracy (test data), and the cumulative strategy. Obviously there are some limits to the comparability, since some models are integrating a split of test and train data and simple models are based on a constraint based approach such as RSI and Bolliger Band.

Following algos are applied:

1.	Bolliger Band
2.	Relative Strengthen Index (RSI)
3.	Logistic Classifier with Grid search and cross validation - pipeline structure
4.	KNN Classifier with Grid search and cross validation - pipeline structure
5.	Recurrent Neural Network (RNN) Simple
6.	Recurrent Neural Network (RNN) with Financial Features and data Split (train/Test)
7.	Density Neutral Network (DNN) with object oriented programming (DNN1 to DNN4)
   
Data Exploration and Viszualization: I conducted a preliminary exploratory data analysis to gain a better understanding of the data and assess its quality. The analysis will primarily involve visualization libraries to gain insights into the data. Plotly will be a useful tool for visualizing the necessary data. To have a complete information set similar to what is available on regular trading platforms, it will be important to create a chart that includes Open, High, Low, Close, and Volume information. In addition to the usual charts such as histograms and line charts, this chart will provide valuable insights into the price trends and trading volume over time.


The price data source and information are as follows:

Oanda Free account / Reuters historical data 2005 to 2023 Brent prices Open, High, low, close and volume Adding additional Plots Lagged price data with a lag of 5 steps For python script we are mostly going to work with a jupyter notebook "exam_script" combined with a "formula_collection.py" script which is saving some helper function to support the main jupyter notebook. 

The Data import is based on "brent_ohlcv.xlsx" with historicals from 2005 to 2023.
Changes to the initial submitted Project: I changed the input Price time series from Oil WTI to Oil Brent since i got the chance to get a time serie from 2005 to 2023 which is way better than intra day move of one month from the WTI. 

I switched in the Sklearn model from the initial Ridge classifier to KNN, since outputs with the other ridge Sklearn model was pretty similar to Logistic classifier. KNN showed very interesting and good results. Simplified the Objection oriented code structure in the last part as code was not running very smoothly on the Callbackfunction - unreliable with hdf5.
Notes to github and google_colab The requirement for the submission of the project is that the .ipynb script runs on "google colab" connected with the publication of the github string /content/EXAM_ALGO/. 

In the first part of the code structre below we need:
Connect to the public script in github Clone https://github.com/neon89/EXAM_ALGO.git including brent_ohlcv.xlsx and formula_collection.py Import with a corrected path the excel data Set up the helper function imports for "formula_collection" with mounting google drive & install ipynb

