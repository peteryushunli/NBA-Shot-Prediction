# NBA-Shot-Prediction
Predicting the outcome of shot attempts in the NBA through Machine Learning Classification modeling: 
For detailed summary of the work, please see the .ipynb file
# Introduction
Inspired by a TEDtalk on NBA analytics, I sought to explore the power of machine learning to predict the result of a shot in the NBA.
Using shot tracking data from the 2016-2017 season, I tested various machine learning prediction models and evaluated results.
# Data
![Preview](https://github.com/yushunli2013/NBA-Shot-Prediction/blob/master/Images/data%20preview.png?raw=true)
# EDA
![Heatmap](https://github.com/yushunli2013/NBA-Shot-Prediction/blob/master/Images/Heatmap.png)

X coordinate has a negative correlation to current outcome, which makes sense because the farther away you are the less likely you will make the basket
![ShotChart](https://github.com/yushunli2013/NBA-Shot-Prediction/blob/master/Images/shotchart.png)

Most teams have similar shot charts. Teams like the Houston Rockets have an emphasis on taking less mid-range shots
# Modeling
## Random Forest Classifier
![rfc](https://github.com/yushunli2013/NBA-Shot-Prediction/blob/master/Images/rfc%20accuracy.png)
## Logistic Regression
![logreg](https://github.com/yushunli2013/NBA-Shot-Prediction/blob/master/Images/logreg.png)
## Gaussian Naive Bayes
![gnb](https://github.com/yushunli2013/NBA-Shot-Prediction/blob/master/Images/gnb.png)
## XGBoost
After performing a series of steps to perform hyperparamter tuning, the best result optained was 42.66% Mean Absolute Error

# Conclusion
Despite trying different models and different levels of hyperparameter tuning, most results averaged around 65% accuracy. This is not incredibly high, but given the data attributes, it is a decent starting point.

There are many additional datafields that would improve the model like:

- Time on the shot clock
- Who is the closest defender
- Distance and angle of closest defender
- Similar datapoints for secondary defenders
- Passes completed before the pass

## Application
I believe with the ceiling of accuracy for such a model would be no higher than 85% and that is largely due to the randomness of NBA basketball. However, a model with 75% or higher accuracy be very useful simulations that can be conducted by teams or betting companies looking to optimize strategy basket-wise or financially, respectively.
