### Problem 2. Suppose that the local power company wants to predict electricity demand for the next 5 days. They have the data about daily demand for the last 5 years. Typically, the demand will be a number between 80 and 400.

#### Describe how you could use an MLP to make the prediction. What parameters would you have to choose, and what do you think would be sensible values for them?

Frame the time-series data as a supervised learning problem using a sliding window approach.
Network will take data from a specific number of past days (k) as input to predict the next 5 days

- Time Delay using consecutive daily data.
- Window size of past data, using the last 14 days to predict the future
- Number of hidden layers and nodes
- Normalization of input data from 80 to 400, scaling the demand values to a range between 0 and 1. Min max scaling.
- 5 output nodes for the next 5 days.


#### If the weather forecast for the next day, being the estimated temperatures for daytime and nighttime, was available, how would you add that into your system?

Add the daytime and nighttime temperatures as extra input features. With window size is 14 days of past electricity data, add 5 daytime temperature input and 5 nighttime temperature input for the forecasted days. MLP model takes 24 inputs to predict 5 outputs.


#### Do you think that this system would work well for predicting power consumption? Are there demands that it would not be able to predict?

It can work reasonably well because it learns patterns from past demand and weather.
Power outages or special events this model will not be able to predict.

