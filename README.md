# Project 2
## Machine Learning in Cryptocurrency Analysis

For project two, we wanted to see if we could predict future closing prices for Ethereum. We selected Linear Regression, Random Forest, Gradient Boosting, XGBoost, Hyper Parameter Tuning, LSTM (Long Short Term Memory), and GRU(Gated Recurrent Units) to determine which algorithm has the best accuracy for outputting the best prediction. 

The first thing we looked into was finding our data. We got our data from yfinance. From here, we can clean the data to make it appropriate for predictions. 

![downloading data and cleaning](https://user-images.githubusercontent.com/94638002/163520388-bb66f14d-5453-4696-a4a0-4cc06cdc263d.png)

After collecting and cleaning the data, the data was graphed. We needed to graph the data so we can copy the graph and put the original data, and the prediction data together into one graph. 

![Graph1](https://user-images.githubusercontent.com/94638002/163520898-dc14d1ee-95d6-4267-8be1-d5bf5195bd65.png)

![Graph2](https://user-images.githubusercontent.com/94638002/163522556-e935358c-61c7-47de-84d0-81d7cc2c2373.png)

One of the issues we had with our data is that it was in a CSV file. In order to make the predictions for the future, we needed to make the data more current. To do this, all the data gets shifted downward using '-1' in each column of the dataframe.

![graph3](https://user-images.githubusercontent.com/94638002/163523948-a23dc113-53c3-49d6-990b-fa13b3858b1f.png)

Next thing to do is evaluate the model to assess its performance. This is done by using 'model.evaluate'. This will show us the test loss and test accuracy. 

![graph4](https://user-images.githubusercontent.com/94638002/163524485-34b0b982-3e41-466c-804a-005c7ade488e.png)

Close to last, we needed to make the predictions. This is done by 'model.predict(X_test)', then print the predicted results.

![graph5](https://user-images.githubusercontent.com/94638002/163524980-c731026e-7d2b-4ac4-aa9a-08a0505fa30e.png)

From here, the predictions have been made. To be able to test the accuracy, we can import metrics from sklearn to print and test accuracy percentages.

![graph6](https://user-images.githubusercontent.com/94638002/163526395-1ca3b620-c210-46cf-87a4-f00e25cc49a0.png)

From here the predictions are complete. In order to keep it up-to-date, we'd need to constantly update the csv file to '-1' each day and reload the code.
