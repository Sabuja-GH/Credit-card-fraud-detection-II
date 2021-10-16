# Credit-card-fraud-detection-II
A hybrid model consisting of SOM and ANNs to predict future frauds at the time of application. 


Hybrid Deep learning model
First unsupervised dl model som to identify the frauds
Then use the results to make a supervised dl model-ann to see the percent a customer can cheat.

When going from unsupervised to supervised we need a matrix of independent variables(features) -exclude ids column include class column

Dependant variable - fraud or not. initialize a zero vector- is_fraud, put 1 in those id places where fraud happed

Use an simple ann becoz we have small dataset like
Remove one, 2nd  hidden layer, units from 6 to 2 in ,input_dim(number of features) =15
X_train=Customers,y_train=is_fraud,batch_size=1,epochs=1 0r 2

Dataset so small/ simple ann model will req 1 or 2 epochs to understand the correlations. so the weights can be updated on those epochs.

Finally, add y_pred and we will convert that y_pred into an array where the first column represents the customer Ids and the second column represent the probability that they are gonna make fraud and at last, we thought the probability column by using .argsort() method 



(dataset.iloc[:, 0:1].values
 2D array  
(dataset.iloc[:, 0].values
vector

