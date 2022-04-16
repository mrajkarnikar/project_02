# Project 2
## Machine Learning in Cryptocurrency Analysis

For project two, we wanted to see if we could predict future closing prices for Ethereum. We selected following algorithms to determine which  has the best accuracy for outputting the best prediction. 
- Linear Regression
- Random Forest
- Gradient Boosting
- XGBoost
- LSTM (Long Short Term Memory)
- GRU(Gated Recurrent Units) 

We also used Hyper Parameter Tuning to come up with best parameter for our model training. Amoung the available hyper parameter tuning methods available we implemented RandomSearch and hyperband. 

## Methodology

The first thing we looked into was finding our data. We got our data from yfinance sdk. We took 2 years of data with daily grain. 

![downloading data and cleaning](https://user-images.githubusercontent.com/94638002/163520388-bb66f14d-5453-4696-a4a0-4cc06cdc263d.png)

After collecting the data, the data was graphed. We needed to graph the data so we can see how the real performance of ETH-USD is.

![Graph1](https://user-images.githubusercontent.com/94638002/163520898-dc14d1ee-95d6-4267-8be1-d5bf5195bd65.png)


From here, we massaged the data to make it appropriate for predictions. We shifted the data  downward using '-1' in each column of the dataframe so that we could use past data to predict future data. We split the data 70:30 and also scaled all the feature data appropriately. 

![graph3](https://user-images.githubusercontent.com/94638002/163523948-a23dc113-53c3-49d6-990b-fa13b3858b1f.png)

Next thing to do was setup the hyperparameter tuning mechanism. We wanted to try out different mechanism for hyper parameter tuning 
Some of the alorigthms we used randomsearch ; but for others we used hyperband. Also, we used different libraries for neural networks. 

Next we set up the model, fit the training data. 

Then we make the predictions. This is done by 'model.predict(X_test)', then print and plot the predicted results.

![graph5](https://user-images.githubusercontent.com/94638002/163524980-c731026e-7d2b-4ac4-aa9a-08a0505fa30e.png)


We then evaluate the model to assess its performance. This is done by using 'model.evaluate'. This will show us the test loss and test accuracy. 

![graph4](https://user-images.githubusercontent.com/94638002/163524485-34b0b982-3e41-466c-804a-005c7ade488e.png)

Close to last, to be able to test the accuracy, we  import metrics from sklearn to print and test accuracy percentages.

![graph6](https://user-images.githubusercontent.com/94638002/163526395-1ca3b620-c210-46cf-87a4-f00e25cc49a0.png)

From here the predictions are complete. 

## Results

GRU
![GRU](./image/GRU.png)

LSTM
![LSTM](./image/LSTM.png)

Random Forrest
![Random Forrest](./image/RandomForest.png)

XGBoost
![XGBoost](./image/XGBoost.png)

Linear Regresson
![Linear Regresson](./image/LinearRegressor.png)

## Conclusion
We concluded that we can somewhat use the different algorithm to predict the future value of eth-usd. However, we realized that the prediction is good only for one day of data. 

We realized that more data necessarily does not mean better models. We also found that newer, complicated models is not necessarily better all the time. It depends upon the use case. For our use case Linear Regression performed the best. 

If we had more time, we would have looked into integrating more features such as inflation data, other crpto data. We would also use other models especially Arima which is known to have better prediction for farther out data. 

We also would have integrated some sentiment analysis using news site and twitter data. 

