# Price-Prediction


## Objective:  
This repository serves as a base model for predicting the closing price of a publicly traded equity.   I believe every model you are create the first step should be to start off with a simple model then expand based off that.  Every quantitative model should have different inputs based on the correlations to it.  

For example:
* John Deere stock would likely correlate to commodity prices (Wheat, Corn, Soybeans, etc.)
* Bank stocks would probably correlate with their respective countries economy, interest rates, employment rate

I also made this program using xgboost (a known algorithm for its speed and performance).  For those who don't know xgboost is an algorithm that continually places at the top of Kaggle (data science competitions).  Rather than use a neural network to start off a new quantitative model, I would instead use xgboost to look at new variables first because of the speed.  

## How It Works:
* A number of inputs are put into the model with the target variable being the closing price
* As the inputs include variables such as (high, low), these would not be inputs would not be known until the end of the day so I set the target variable to be seven days into the future
* Note: I didn't add macroeconomic indicators to this base model because I want the code to be easily adapted to predicting commodities or indexes. 

## Technical Indicators:
* MACD: Moving Average Convergence/Divergence Oscillator, for a momentum indicator
* RSI: Oscillators help identify overbought and oversold markets
* ADX: determine whether a market is in a trending or trading phase.  It measures the degree of trend or direction in the market
* Average True Range: measure of volatility
* Exponential Moving Average

## Feature Importance:
![picture](Base_Model_Feature_Importance.png)

## Results from a sample company (Netflix): no unique features added
*  It should be noted that stocks with a higher beta will likely need more inputs to correctly predict the price
![picture](BaseModel_Results.png)

## After some features were added to the Netflix model
![picture](nflx_model_updated.png)

