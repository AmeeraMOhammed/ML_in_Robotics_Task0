# ML_in_Robotics_Task1
## Packages used
### First: The model implemented from scratch
* NumPy: it provides support for multi-dimensional arrays usage and some mathematical functions.
* Matplotlib: plotting library used for visualizations.
* Pandas: is a data manipulation library that offers functions to work with files as CSV files or Excel sheets.
* Seaborn: is a data visualization library based on Matplotlib used for creation of visually appealing statistical graphics (used for the correlation graph).
### Second: The model implemented using sklearn library
* NumPy: it provides support for multi-dimensional arrays usage and some mathematical functions.
* Matplotlib: plotting library used for visualizations.
* Pandas: is a data manipulation library that offers functions to work with files as CSV files or Excel sheets.
* Seaborn: is a data visualization library based on Matplotlib used for creation of visually appealing statistical graphics (used for the correlation graph).
* Linear regression fron sklearn.linear model: The Linear Regression class in scikit-learn is a machine learning estimator that implements linear regression.
* The train_test_split: function used to split the given dataset into training data and testing data to evaluate the model performance.
* The r2_score function: is a utility function from the sklearn.metrics known as the R-squared score, for a regression model. The R-squared score is a measure of how well a model fits the data by comparing the predicted values to the actual values.

## Problem definition
Task 01 folder includes two notebooks both for linear regression model applied to insurance dataset in order to predict the insurance charges based on many features as smoker, bmi and age (features that show largest correlation), the first one implemented using sklearn library and the second one implemented from scratch using python only.
## Code flow
### First: The model implemented from scratch
Import the necessary libraries as: numpy for arrays and numerical operations, matplotlib.pyplot for plotting, pandas for data manipulation, and seaborn for visualization.

Import the file from its directory to the insurance dataset and read it into a df (pd.read_csv()).

Data preprocessing by converting the values inside (sex, smoker, and region) from string to numerical data.

Find the correlation and the strength of each feature in the target (charges) and representing it in a plot using seaborn library in a form of heat map (sns.heatmap()).

Displaying the correlation (plt.show()).

Selecting certain features (age, bmi and smoker depending on the correlation plot as smoker, age and bmi showed the greatest contribution in the target (charges), smoker contributes by 79% in the charges, age contributes by 30% in the charges, and bmi contributes by about 20% in the charges and the others showed very low contribution that they could be ignored.

Convert the x and y data to NumPy arrays using np.array().

Adding ones column to x to account for the bias term (b) (np.column_stack()).

Splitting the data into training and test sets manually where 80% is used for training and only 20% for testing.

Defining the linear_regression() function that performs linear regression.

Training the linear regression model.

Calculating the R-squared value from scratch by computing the total sum of squares, residual sum of squares, and subtracting the ratio from 1.

Printing the calculated R-squared value.

A scatter plot to compare the predicted insurance charges with the real insurance charges.

### Second: The model implemented using sklearn library
## Comparing between results of scikit-learn library and its implementation from scratch 
the results from the following model varies from that of the model created using sklearn.
as we see the value of the r-squared is 0.7563721013596153 which means about 75.63% accuracy while the value of the r-squared value from the other model is 0.7945500805653087 which is about 79.455% accuracy more than the implemtation from scratch.
## Author:
* Name: Amira Mohamed Abd El-fattah
* Section: 1
* B.N: 15
