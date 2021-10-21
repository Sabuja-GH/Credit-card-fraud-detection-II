# Credit-card-fraud-detection-II
A hybrid model consisting of SOM and ANNs to predict future frauds at the time of application. 

In this hybrid deep learning model, first unsupervised DL model SOM is used to identify the frauds then we use the results to make a supervised DL model- ANN to see the percentage that a customer can cheat.

We will continue from where we left the Credit card fraud detection-I.

* When going from unsupervised to supervised we need a matrix of independent variables(features) -exclude ids column include class column.

* Dependant variable - fraud or not. Initialize a zero vector- is_fraud, put 1 in those id places where fraud happened.

* Use an simple ANN because we have a small dataset.
  * Only one hidden layer, 2 units/nodes/neurons (enough to extract features)
  * input_dim(number of features)= 15
  * X_train=Customers,y_train=is_fraud,batch_size=1
  * batch_size= 1 0r 2

*Dataset so small/simple our ANN model will require around 10 epochs to understand the correlations. so the weights can be updated on those epochs.*

* Finally, predict y_pred and we will convert that y_pred into an array where the first column represents the customer Ids and the second column represent the probability that they are gonna make a fraud.
* At last, we sort the array according to the probability column by using .argsort() method.


> (dataset.iloc[:, 0:1].values)-
 2D array 
 
> (dataset.iloc[:, 0].values)-
vector
