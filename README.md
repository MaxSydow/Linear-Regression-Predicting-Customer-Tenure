# Predicting Customer Tenure Using Linear-Regression

It is a common adage in the telecom industry that it costs more to acquire new customers than it does to keep existing ones. It would be worthwhile to look at which factors affect how long a customer keeps their services with an ISP, an attribute called Tenure. The Customer Churn data set contains 50 descriptive columns of numerical and categorical data which describe characteristics of customers, their services, and sentiments regarding the ISP. Some of this data may be useful in predicting Tenure. Multiple linear regression can be used to examine how columns, as explanatory variables, affect the Tenure outcome variable.

[Method Justification and Assumptions](#method-justification-and-assumptions)

# Objectives and Goals:




Performance characteristics of such a model can be examined and used to find which explanatory variables make for better predictions. There are so many variables to start with, and surely using all 49 to predict just one would not be the best idea. Issues such as overfitting and co-linearity can hinder model performance. A good predictive model will be able to make predictions on non-existing data. Overfitting occurs when there are too many data points making the predictions overly specific to the variables that the model was created with. An entire column could result in overfitting too, and P-values for columns in a model can be used to look at which suggests changes in the predicted variable that are not associated with changes in the explanatory variables. Collinearity occurs when there is a strong linear correlation between explanatory variables. Regression coefficients and residuals can be used as quantifiable measures of a model’s accuracy. There may also be some explanatory variables that can just be eliminated using domain specific knowledge and narrowing the scope of the model. The goal, then is to use all of these techniques to end up with a model with an optimum collection of explanatory variables that gives the best predictions for Tenure.

## Method Justification and Assumptions
Summary of Assumptions
The outcome of multiple linear regression is a linear equation of the form

Y = b + a1x1 + a2x2 + … + anxn,

where Y is the target, or response variable, b is an intercept, the xi’s are the explanatory variables, and the ai’s are coefficients. The equation is essentially a multi-variable analog of the common equation for a line in 2-dimensions:

y = mx + b.

Each of these elements should be numeric. More specifically the predictive variable needs to be numeric and continuous, but the explanatory variables can be discrete and numeric. The equation can be found by minimizing the differences between actual data points and a theorized best prediction or expectation. Such expected values can be expressed in the same form as the linear equation above, where E(Y) is used to denote the expected value of the response variable. Residuals are the differences between actual data points and the expected values. The regression model depends on minimizing the set of residuals.

Tool Benefits
In a single variable model finding the smallest residuals can be found by hand using calculus, but the calculations become unwieldy with a larger number of variables. Programming languages come in handy here. Python has several pre-coded packages that contain useful functions for model creation and exploration. Data sets can be stored in objects like data frames and arrays and used for input and output with these functions. Jupyter Notebooks is a commonly used Python platform that allows for execution of smaller chunks of code in cells. This makes it easier to navigate the code of a project, and to trouble shoot smaller pieces of it. Each cell can be used to accomplish a specific objective of a project and present it in a clear sequential manner.

Appropriate Technique
The Churn dataset contains columns with categorical data. Some of these columns might be useful in making predictions but can’t be treated mathematically. When columns consist of Yes or No values, they can easily be transformed to 1’s and 0’s. Likewise, columns with a higher number of categories can be mapped to numbers counting up to how many discrete values there are in them. Once this is done a collection of numeric explanatory variables can be stored in a data frame along with a continuous response variable. The Tenure column contains numeric continuous data, so multiple linear regression using Python can be used to create predictive models.
