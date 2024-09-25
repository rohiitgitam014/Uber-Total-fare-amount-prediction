Uber Total Fare Amount Prediction


Project Overview
This project aims to predict the total fare amount for Uber rides based on various factors such as trip duration, distance traveled, number of passengers, and additional fees. Using a dataset with over 200,000 records, we developed a machine learning model to accurately predict the total fare, leveraging data exploration and a linear regression model.

Data Overview
The dataset consists of 209,673 Uber ride records, with eight features, including:

trip_duration: Duration of the trip (in seconds)
distance_traveled: Distance covered during the trip (in miles)
num_of_passengers: Number of passengers
fare: Base fare amount for the trip (in dollars)
tip: Tip given by the passenger (in dollars)
miscellaneous_fees: Any additional fees such as booking or service charges (in dollars)
total_fare: The final fare charged to the passenger, including all fees and tips (in dollars)
surge_applied: Whether surge pricing was applied (Yes/No)
The dataset is free from missing values, making it ideal for model training without the need for imputation.

Data Exploration and Visualization
To gain insights into the relationships between different variables, several visualizations were created:

A bar plot was used to analyze the relationship between surge_applied and total_fare, revealing the impact of surge pricing on the fare amounts.
A scatter plot highlighted the strong positive correlation between fare and total_fare, which indicates that base fare is a major driver of the total fare.
A correlation heatmap showed that:
fare has the highest correlation with total_fare (0.97).
tip and miscellaneous_fees also contribute positively to total_fare, though to a lesser extent.
These visualizations helped identify which variables were most relevant for predicting the total fare.

Modeling Approach
We used Linear Regression, a popular algorithm for regression tasks, to predict the total fare. The process followed these steps:

Data Preparation:

The dataset was split into training and testing sets, with 70% used for training and 30% for testing.
The target variable was total_fare, and the primary predictor used was fare, as it had the highest correlation with the target.
Model Training:

The model was trained using the LinearRegression class from the scikit-learn library.
After training, predictions were made on both the training and test sets to evaluate the model’s performance.
Model Evaluation:

The model achieved an R² score of 93% on both the training and test data, indicating a high level of accuracy in predicting the total fare.
The residuals (difference between predicted and actual fare values) were analyzed using density plots. The residuals were centered around zero, demonstrating that the model made accurate predictions with minimal error.
