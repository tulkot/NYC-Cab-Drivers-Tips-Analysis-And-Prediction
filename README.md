# NYC-Cab-Drivers-Tips-Analysis-And-Prediction
New York City has millions of taxi trips taken every month. This project aims to make an analysis and form a better understanding of the New York City Taxi tips data. Cab drivers are often tipped after a ride apart from the base fare amount for the trip. A tip is essentially an additional fare given to a driver, post a trip. 

### The Data
The dataset used for this project will be obtained from the NYC Govt. website, from the Yellow Taxi Trip Records from 2021. The aim was to look for Uber/Lyft datasets having tips as a feature in the dataset, but those are unavailable on the Internet, hence the NYC YellowTaxi dataset.

Source Link: https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page

The dataset has features like pick-up and drop-off times, pick-up and drop-off locations, trip distance, passenger count, payment type, fare amount, tip amounts, etc. The dataset chosen is from January 2021, and one month alone has about 1370000 records. To perform a comparative analysis, a month of summer could also be added to the dataset (any of June-August), and/or a comparative analysis between the holiday season months and non-holiday season months.

The original dataset has 19 columns including the tip_amount column, and datasets of January 2021 and June 2021 were taken to create a comparative analysis between the tipping behavior during holidays and non holidays season, and during the climatic seasons(Winter, Summer).

### Ordinary Least Squares Regression and Gradient Boost Regression
This section will build two regression model to predict the tip amount for eligible taxi trips. Model fit is evaluated using the train-test split method to randomly split sampled data into 80% training set and 20% testing set. Initial feature selection is done by inspecting the correlation plot to drop redundant predictors to avoid overfitting.

### Evaluation
The fitness of the models are evaluated in terms of Root Mean Square Error and Coefficient of determination R2. Result of our models are compared against the baseline model that only contains the intercept, which simply used the mean as the predicted value.

### Analysis Results
In conclusion, through some exploratory analysis of yellow taxi trip records, the relationship between some attributes has become a lot more clearer. The performance of the model is affected due to the heavily right-skewed distribution of tip amount, as a large portion of tip amount are clustered at a very low value between $0 and $7. weekdays are usually the busiest, especially at the evening rush hours; late-night pickup frequency is generally higher over the weekend, possibly due to people’s late-night activity. As for tipping, passengers tend to tip less generously in the early morning and evening rush hours, and tipping percentages are higher during the day between 10 am to 3 pm and at night between 8 pm to 10 pm.
