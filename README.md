# Group Project Final Report (Group 11)

## Introduction
### Background Information
As digital payments boomed in recent years with the rapid development of the Internet, people enjoy the fast and convenient transaction service but also face an increasing number of cyber criminals alongside. The Data Breach Index announced that over five million records are being stolen on a daily basis, which indicates that fraud is very common in our daily life. However, detection of fraud is challenging since trillions of card transactions happen per day.

### Research Question
Using our classification model, can we predict fraudulent transaction using **distance from home and ratio to median purchase price** variables to prevent future crime?

### Dataset description
We will be using a dataset called Credit Card Fraud by Dhanush Narayanan from https://www.kaggle.com/datasets/dhanushnarayananr/credit-card-fraud. The dataset is in a “Comma Seperated Value” (csv) file format and contains eight columns, which are:

distance_from_home = the distance from home where the transaction happened.   
distance_from_last_transaction = the distance from last transaction happened.  
ratio_to_median_purchase_price = Ratio of purchased price transaction to median purchase price.  
repeat_retailer = whether the transaction happened from same retailer or not  
used_chip = whether the transaction is through chip (credit card) or not  
used_pin_number = whether the transaction happened by using PIN number or not  
online_order = whether the transaction is an online order or not  
fraud = whether the transaction is fraudulent or not  

Our target variable, which is the variable that we are predicting, is fraud and the predictors that we will be using are distance_from_home and ratio_to_median_purchase_price.  

### Methods & Results
To conduct our analysis, we will load the dataset into R, find the correlation between fraud and other variables, and clean and wrangle the dataset into a tidy format. We will use fraud as our target variable and our predictors are ratio_to_median_purchase_price and distance_from_home as they have the highest correlation to fraud. We will then determine the value of k that has the highest estimated accuracy by cross validation and train our model using the best value of k. Lastly, we would use our classifier to make predictions on the testing dataset and some new observations, and evaluate its accuracy. The final step is to visualize our analysis by creating a colored prediction map where we plot ratio_to_median_purchase_price VS distance_from_home, separate types of transactions using different colors, and represent the predictions using coloured areas. We will also visualize how the predictions compares with the true labels of the testing dataset.
