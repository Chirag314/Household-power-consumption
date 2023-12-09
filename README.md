# Household-power-consumption
Time series data analysis practice

Household Power Consumption Prediction with LSTM
The script starts by importing necessary packages:

math for mathematical operations
tensorflow and keras for building and training the LSTM model
tensorflow.keras.utils.Sequence for creating custom data generator
datetime for handling date and time
sklearn.preprocessing.MinMaxScaler for data normalization
sklearn.metrics.mean_squared_error for calculating the mean squared error
numpy for numerical computing
pandas for data manipulation
time for time-related functions
os for operating system functionalities
seaborn for data visualization
warnings for suppressing warnings
2. Data Preprocessing

Reading the data: The script reads the household power consumption data from a CSV file named household_power_consumption.txt.
Missing values: Missing values in the Global_active_power feature are removed.
Feature engineering:
date_time feature is created by combining the Date and Time columns.
year, quarter, month, day, and weekday features are extracted from the date_time feature.
weekday is encoded as 1 for weekdays and 0 for weekends.
3. Data Exploration and Analysis

Descriptive statistics: The script analyzes the data using various statistical methods:
Checks if the data follows a normal distribution.
Prints information about the data types and missing values.
Shows the first 10 rows of the data.
Time series plot: The script plots the time series of the Global_active_power feature.
Box plot: The script creates box plots to compare the distribution of Global_active_power across different years and quarters.
Distribution plot: The script plots the distribution of the Global_active_power feature and checks for normality using a Q-Q plot.
Resampled plots: The script plots the average Global_active_power resampled over various time intervals (day, week, month, quarter, and year).
Mean plots: The script plots the mean Global_active_power grouped by year, quarter, month, and day.
Year-wise plot: The script plots the annual average Global_active_power for each year.
Weekdays vs. weekends: The script compares the Global_active_power consumption on weekdays and weekends using box plots and factor plots.
Stationarity test: The script tests the stationarity of the Global_active_power time series using the Augmented Dickey-Fuller test.
4. LSTM Model for Power Consumption Prediction

Data preparation:
All data is converted to float format.
The data is normalized using MinMaxScaler.
The dataset is split into training and test sets.
A custom data generator is created using the create_dataset function to create sequences of data for training the LSTM model.
Model definition: A LSTM model is defined with the following parameters:
Look back window of 30 days.
One LSTM layer with 50 units.
Dense output layer with one unit for predicting the next day's power consumption.
Model training: The model is trained on the training set using the mean squared error as the loss function and the Adam optimizer.
Model evaluation: The model's performance is evaluated on the test set using the mean squared error.
5. Conclusion

This script demonstrates a complete analysis and prediction of household power consumption using an LSTM model. The script provides detailed visualizations and statistics to understand the data and evaluate the model's performance.

Additional Notes:

The script includes Python comments for better understanding.
The script uses various libraries for data manipulation, visualization, and modeling.
The script can be further improved by optimizing the model architecture and hyperparameters.

