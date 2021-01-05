# simple-stock-classifier
This project shall explore the steps involved in building a stock recommendation classifier.

Motivation: I selected this project because mastering the stock market is an age-old question whose answering is saught after by many. This project will try to use a supervised ML model to predict whether the stock will go up or down in any given day.

*Dislaimer: This model should not be used as trading or investment advice. All investments are subject to market risks and investments should be made considering the said risks. This is for educational purposes only*

Libraries used in the project:
  pandas==1.0.1
  numpy==1.18.1
  matplotlib==3.1.3
  seaborn==0.10.0
  yahoofinancials==1.5
  scikit-learn==0.22.1


Files Description: This project include stock_recommendation_classifier notebook which details all the codes and analysis done to build the classifier

Project summary:
Business use case: Since the advent of financial markets, humankind is trying to predict the market in order to have market psychology work in their favor.
As technology is getting more and more advances, we have unprecendent computational power to uncover hidden patterns in financial data which were eluded to 
traders up til today. The purpose of this project is to harness this computing power by building ML classifier to predict whether a stock will go up or down
at any given day. This is particularly useful for investment managers so that they can have better predicting power in their investment management practices.
In order to support our use case, we will attempt to find the answers of the following questions:
Q1-Whether historical price and volume data can serve as potential features to predict the respective stock prices?
Q2-Whether overall historical stock market volatility has any correlation with the price data of a given stock and hence whether can be used as a feature as well?
Q3-Whether we can use supervised ML classifier Models to predict whether the stock price will go up or down on any given day?

Data Understanding: Here we used use Yahoo! Financials API to fetch Google's historical daily pricing ('OHLC') data. This data also included volume information.

Preparing Data: We found that data did not have any missing values. However, while making features we had some NaN values which we dropped later. We also had to scale the data to arrive at better predictions.

Data Modelling: We constructed a correlation matrix among the features to check whether prior pricing information had any correlation with future prices and we found that there was a strong correlation among them which answered our Q1 that past historical data can infact serve as a potential features to predict prices. While we also found negative correlation between market volatility and historical price and hence market volatility can be used as a feature as well. This answered our second question as well. And once we build our classifier model we noted that we got a decenct accuracy on validation sample which should that classifier models can be potentially used to predict stock movement.

Results: We saw that there was some alpha in using ML models in your investment management process.
