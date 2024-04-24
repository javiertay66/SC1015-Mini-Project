# SC1015-Mini-Project - Prediction of Gold Price
## Repository Description
This Repository is submitted to Nanyang Technological University as part of a graded assignment for SC1015 (Introduction to Data Science and Artificial Intelligence which focuses on the prediction of gold prices.
## Dataset used
Our dataset is from Kaggle: "2019-2024 US Stock Market Data" by Saket Kumar
Source: https://www.kaggle.com/datasets/saketk511/2019-2024-us-stock-market-data

This dataset offers an intricate exploration of market dynamics spanning five years (2019-2024). It represents a valuable dataset for dissecting trends and patterns within the global markets.

## Table of Contents:
  1. Problem Formulation
  2. Data Preparation and CLeaning
  3. Exploratory Data Analysis
  4. Machine Learning
  5. Data-Driven Insights and Conclusion

## 1. Problem Formulation
   -To explore the relationship between different commodities/indexes.
   -To find out which commodity/index serves as the best predictor for Gold Price
   
## 2. Data Preparation and Cleaning
In this section, we cleaned and prepared the dataset to help us analyze our data better. This also ensures that our data is accurate, complete and consistent to prevent any errors further down the road. This will allow us to draw reliable conclusions, make informed decisions and avoid misleading insights. We removed unneccessary columns in the dataset, checked for duplicate entries and checked for null values in our dataset.

## 3. Exploratory Data Analysis
For this section of our project, we first did a preliminary exploration where we plotted the correlation matrix to find out which stocks to choose and use to predict gold prices. After carefully analyzing the results, we chose the following 3 predictors: Nasdaq_100_Price, Apple Price and Silver_Price, where we picked one predictor from each asset classes which seem to have a high correlation with Gold Price so that we do not "overcommit" to one asset class.  We then found out the statistics for each stock and we plotted a time series graph and a scatter plot showing the stock's correlation with gold price to better understand these predictors.

## 4. Machine Learning  
   1. Linear Regression
   2. Seasonal Autoregressive Integrated Moving Average Model (SARIMA)
   3. Random Forest Classification
We first applied Linear Regression to compare each of the predictors and choose the most suitable predictor for gold price, which is Apple Price. Next, we incorporated the SARIMA model with Apple prices as an exogenous variable. Apple prices can provide additional insights that can help SARIMA model better capture the relationships between gold and apple prices, thus improving the accuracy of predicting future gold prices. Lastly, we used Random Forest Classification to classify whether to buy gold or not based on the following condition: If Apple_Price increases for 2 days consecutively, we will classify as 'Buy" and vice versa.

## 5. Data-Driven Insights & Conclusion
From our analysis, we found that Apple stock price has the highest correlation coefficient with Gold prices, lowest Mean Squared Error(MSE) and highest R^2. Hence, we chose Apple price as the predictor for Gold prices. 

The dataset actually tells us that there are many stocks we can use to predict Gold prices and hence choosing the most suitable one is essential for optimal accuracy. Using the prediction models like the random forest classification, we can see a relatively high accuracy. Thus, we think that it is indeed possible to predict future gold prices. However, it is important to be wary that the prediction models are not 100% accurate. We should not entirely depend on such models to strike it rich overnight. There are high risks in investing in gold as the fluctutations are hard to predict.

Overall, our model is particularly good at predicting when not to enter the market to buy gold, evident by the high True Positive Rate and low False negative rate as seen in our confusion matrix. Hence, our model will prove useful to risk-averse investors who might have qualms about investing.

## Contributors
School of Computer Science and Engineering, NTU Singapore
AY2023/24 SC1015 ECDS1 Group 6

JAVIER TAY YU XIANG JTAY091@E.NTU.EDU.SG
JARED ONG KAI ZE 
ERNEST THEN SHI SHENG ETHEN003@E.NTU.EDU.SG
