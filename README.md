# machine_learning
Implementation of supervised learning, unsupervised learning, and reinforcement learning models.

This file demonstrates how to implement linear regression. 
Linear regression can be of two different types. The first one is simple linear regression, where there's one dependent and independent variable. The second one is multiple linear regression, where there's one dependent variable and multiple independent variables. We can use regression to predict the value of dependent variables or outcomes.

This file focuses on the implemention of regression without using any external libraries,but just the core Python.

Now in order to calculate linear regression, we need to understand certain statistical methods. The first method that we're defining in line 5 is mean.
Mean is the calculation of the mean value on a given list of numbers. And as such, it takes values as parameters, and it returns the sum of values divided by the total number of values, which is specified in line 6.

The next statistical method that we need to understand is variants, which is basically a measurement used to identify how far each number in the data set is from the mean. When researching variance is useful, as we can use it to calculate the probability of future events. Or in other words, variance is useful for facilitating predictions. 
Numerically, if the value of variance is zero, it would mean that all the value within the dataset are identical. While all variances are not equal to zero, it will come definitely in positive. 
In other words, the larger the variance, the larger the spread is, which is basically the distance among the data in the dataset. Now in order to calculate the variance, we've defined a function in line 9.

The variance is calculated by taking the difference between each number in the dataset and the mean. Following which, we'll square the difference to return a positive value. So in line 9, we've specified the function covariance to calculate the covariance. And we're passing x and y followed by the mean of x and y. 
We're using an assumption that the covariance is equal to 0.0 in order to initialize the covariance variable.

Then we're going through the dataset by using a loop in line 11,Then we're going through the dataset by using a loop in line 11,

We're calculating the covariance, which is equal to the difference between the number. For example, x[i] and the mean of x, then we're multiplying it with the difference in the variable and the mean of y, which is y[i]- mean_y. 
After the loop is executed, we'll get a summation of the covariance that we applied on each data which is present in the dataset. And on line 13, we're returning the covariance.

We've also defined the variance, which calculates the difference and the mean squared, as specified in line 17.
So the mean of the covariance and the variance are going to play an important role, as it will help us in defining the linear regression and predicting the outcome by a final linear regression. 

The next calculation is the coefficient, which is a term used to refer to the resulting correlation measurement. In order to calculate the coefficient, we have to define a method in line 20, which takes a dataset. Then we're using two variables, x and y, which will retrieve the data from the dataset using a loop which we have specified in the arrays. So x will be an array of all the data from row 0 in the dataset, and y will be another array, which will be retrieved from the dataset at the index row 1. 
So whenever a dataset is passed to the coefficient, we'll calculate x and y to derive the content of x and y from the dataset. We're also calculating the mean of x and y. Where the mean value is the total sum of x array divided by the total number of values of x. 
The same applies for the means of y, where the mean value is the total sum of y array divided by the total number of values of y.

Then we're calling the method covariance in line 24.
The covariance has already been defined in line 9. To this method, we're passing x, x_mean, y, y_mean, and we're dividing it with the total variance of x and x_mean. This will provide the value of x1, which is the coefficient. The other value of coefficient is x0, which is calculated as y_mean- x1, which is the previous covariance, multiplied by the x_mean. Now after specifying the methods for mean, covariance, variance, and coefficient, we can begin applying the linear regression algorithm. 

In line 38, we've defined the method simple_linear_regression,which takes two values. The first one is train, which is the training dataset. And the second one is test, which is the testing dataset. In line 39, we declared the variable prediction, which is the type of list.

In line 40, we're calculating the coefficient, which returns b0 and b1, then we're iterating in the row to calculate the value of yhat.
Now the value of yhat provided by the sum of b0, b1, which is in turn multiplied with the row[0], will append this prediction in the list.

When the loop has executed, it will return the prediction. We will also calculate the root mean squared error, which will help us to identify the distance between the actual and predicted value. For this calculation, we have to calculate the sum of error. The sum of error is calculated by iterating in the actual value, which we've passed to the rmse_prediction function in line 29.

In line 30, we've defined the function passing as the actual and predicted value. Following which, we calculate the sum of error by iterating the actual value.

In lines 32 & 33, we've defined the function passing as the actual and predicted value. Following which, we calculate the sum of error by iterating the actual value.

In line 34, we will apply this for all values in the array and we'll calculate the sum_error. After we get the sum_error, we have to calculate the mean_error by dividing the total sum_error by the total
number of actual value that we used earlier to calculate the sum_error. And we'll apply root mean squared error.

In line 35, the calculation will return the root mean squared error. So far, we've specified the simple regression, the rmse_prediction, which helps us in calculating the square root of the mean error. Now we have to declare another function which is responsible for prediction. We can facilitate the prediction by applying certain algorithm on the dataset. 
So on line 48, we're defining a function which can manage predictions, and we're passing dataset and algorithm.

On line 49, we're declaring an empty test_set. 
We're iterating in the dataset. We're taking a copy of that row, we're passing an index to the row, and finally, we're copying the particular row_copy, which we specified in line 51 to our test_set.

So using the dataset, we're building the test_set. Now after creating the test_set, we have to facilitate the prediction using the test_set. So on line 54, we're calling a function, which is passed as an argument in line number 48 for the method manage_prediction.

The algorithm is applied on the dataset and test_set, then we're printing the predicted value. After we have accumulated the predicted value, the next task is to return the rootmeansquaredError. And we've already defined a method for the same in line 29. So on line 56, we're declaring the variable actual.

And we're iterating in the variable by creating an array of values within the actual variable. On line 57, we're calculating the rootmeansquaredError using the method rmse_prediction, for which we're passing actual and predicted.

The function, which is defined in line 29, will be executed, get the data, subtract it from the actual and return the rootmeansquaredError. So the method manage_prediction is taking the responsibility of applying regression on the dataset and return the rootmeansquaredError. Now we can test the functions that we've specified in the program so far. And in order to test the functions, we need a dataset. And we also need to specify the algorithm, which is already defined in line 38. 
In line 62, we're preparing the dataset, which contains a combination of two values, since we're using simple regression. They're dependent and independent. The dependent dataset contains an array of the dependent and independent variables. Now that we have prepared the dataset and defined the algorithm in line 38, the next task is to call the method manage_prediction, which we specified in line 63.

We're passing the dataset followed by the algorithm that we've defined. And when the method executes, it will return rootmeansquaredError. Finally, we will print the rootmeansquaredError.

We can test the program by running it.

The console displays an array, which is a predicted value, followed by the root mean squared error, which is 7.3, and this value helps us identify the accuracy of the algorithm. And this is how we will implement simple linear regression with core Python rather than using any predefined libraries.
