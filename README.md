# Litecoin-Bitcoin-Gradient-Descent
I was doing some research on Deep Learning, and stumbled upon very interesting concept of Gradient Descent.

The following code is an example of how Gradient Descent works to find a Regression line.

Quick recap for Linear Regression: The aim of Linear Regression is to find a regression line such that:

y_hat = mx + b

ie. we can predict the value of y for any x once we have the variables m and b (the slope and the intercept of the regression line)

Gradient Descent is basically a mathematical optimization to reach the local minima of our loss function. It works as follows:

1) At every value of the weights, we find the predicted value using that weight. 2) Then we find the error using a loss function. In this example, I've used the Mean Squared Error. 3) Once we know the error, we tune the weights such that the error is minimized. Our goal is to achieve the minimum error, which is the local minima. (for convex functions, local minima = global minima) 4) To know whether to increase or decrease the weight to achieve this minimization, we use partial derivatives. The partial derivative of each parameter gives us a direction in which we need to tune the weights. 5) We tune the parameters by changing their values with respect to the values of the partial derivatives. 5) The tuning stops once the partial derivative value is 0, that is, local minima is achieved or the most optimal weight is found.

The model here is used to predict Litecoin prices based on Bitcoin prices. The dataset I've used is from Kaggle, and contains LTC, BTC prices from April 2013 till September 2017.

We find a almost 100% positive correlation in the two variables. The intercept b has a miniscule value of -0.00005 with a slope of 0.013, rightly so, since LTC prices are much lower than BTC.
