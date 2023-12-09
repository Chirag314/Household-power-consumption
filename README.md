# Household-power-consumption
Time series data analysis practice

Readme for Household Power Consumption Prediction with LSTM
This readme provides a step-by-step guide for the code used to predict household power consumption using an LSTM model.

Data Exploration and Preprocessing
Import Packages: The code imports necessary packages like TensorFlow, Keras, NumPy, Pandas, etc.
Read Dataset: The household_power_consumption.txt dataset is read using Pandas.
Convert Features: Features are converted for better analysis.
date_time is converted to datetime format.
Global_active_power is converted to numeric type and missing values are dropped.
Additional features like year, quarter, month, day, weekday are created from the date_time feature.
Data Exploration:
The number of rows and columns is displayed.
The time series range (start and end date) is printed.
Normality of the data is checked using Shapiro-Wilk test.
Descriptive statistics of the data are displayed.
Time series plot is created to visualize the trend of global active power.
Boxplots and violin plots are used to compare power consumption across different years, quarters, months, and days.
Stationarity Analysis:
Rolling mean and standard deviation are plotted to check for stationarity.
Augmented Dickey-Fuller test is performed to confirm stationarity.
LSTM Model for Power Consumption Prediction
Data Conversion:
All data is converted to float.
Global active power feature is normalized using MinMaxScaler.
The data is reshaped into a suitable format for LSTM input.
Training and testing data are split.
Dataset Creation:
A function create_dataset is defined to create sequences of data for training and testing.
The function takes the dataset and look_back period as input.
It returns the input (x) and output (y) sequences for training and testing.
LSTM Model Building:
An LSTM model is built using Keras with one LSTM layer and one Dense layer.
The model is compiled with mean squared error as the loss function and Adam optimizer.
Early stopping is used to prevent overfitting.
Training and Evaluation
Model Training: The LSTM model is trained on the training data for a specified number of epochs.
Model Evaluation:
The model's performance is evaluated on the test data using mean squared error.
Predictions are made on the test data and compared with the actual values.
Results and Conclusion
The readme should summarize the results of the experiment, including:

The final model performance on the test data (MSE).
Comparison of the model's performance with other models (if any).
Key insights and conclusions drawn from the analysis.
Dependencies
TensorFlow
Keras
NumPy
Pandas
Matplotlib
Seaborn
Scikit-learn
Additional Notes:

This is just a basic structure for the readme. You can add more details and customize it according to your specific analysis and findings.
Include screenshots or plots of the generated results to visually represent the findings.
Provide references to any external resources used in the analysis.
Make sure the readme is well-organized and easy to understand for readers with different levels of technical expertise.
