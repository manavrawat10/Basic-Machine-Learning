Simple Linear Regression
========================

Simple linear regression is an approach for predicting a response using a single feature.

It is assumed that the two variables are linearly related. 
Hence, we try to find a linear function that predicts the response value(y) as accurately as possible as a function of the feature or independent variable(x).

Now, the task is to find a line which fits best in above scatter plot so that we can predict the response for any new feature values. (i.e a value of x not present in dataset)

This line is called regression line.

Here,

    y_pred = b[0] + b[1]*x

y_pred represents the predicted response value for ith observation.
b_0 and b_1 are regression coefficients and represent y-intercept and slope of regression line respectively.
To create our model, we must “learn” or estimate the values of regression coefficients b_0 and b_1. And once we’ve estimated these coefficients, we can use the model to predict responses!

In this article, we are going to use the Least Squares technique.

So, our aim is to minimize the total residual error.

our task is to find the value of b_0 and b_1 for which J(b_0,b_1) is minimum!

Without going into the mathematical details, we present the result here

b_1 = SS_xy / SS_xx

b_0 = m_y - b_1*m_x

where SS_xy is the sum of cross-deviations of y and x
	
  SS_xy = np.sum(y*x - n*m_y*m_x)
	
and SS_xx is the sum of squared deviations of x

  SS_xx = np.sum(x*x - n*m_x*m_x)
  
Note: The complete derivation for finding least squares estimates in simple linear regression can be found here.
