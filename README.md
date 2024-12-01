# Time-Series-Analysis-of-TATA-Motors

# Overview
The primary goal of this project is to predict the future stock prices of TATA Motors using Deep Learning technique. By leveraging time series forecasting, this project aids investors and analysts in making informed decisions.

# Dataset
- **Source:** Data was collected from the Bombay Stock Exchange (BSE) website.
- **Time Period:** April 2017 to December 2022.
- **Features:**
   - Date
   - Open
   - High
   - Low
   - Close
   - Adjusted Close
   - Volume

# Preprocessing
- Converted the Date column to a datetime format and set it as the index.
- Selected the Close column for analysis.
- Scaled the data using MinMaxScaler to normalize values between 0 and 1 for better model performance.
- Split the data into training (80%) and testing (20%) sets.

# Data Visualization
- Visualized the closing price trend using matplotlib.
- Performed seasonal decomposition using statsmodels to observe trend, seasonality, and residual components.

# Models Used
# Auto ARIMA
- Used pmdarima.auto_arima for automatically determining the best ARIMA model parameters.
- Split data into training and test sets (80/20 ratio).
- Forecasted stock prices over the test period and plotted the results with confidence intervals.

# LSTM Model
- Two LSTM layers with 50 neurons each and return_sequences set appropriately.
- Dropout layers for regularization.
- Dense output layer for regression tasks.
- Used a time step of 60 (previous 60 days) to predict the next day's stock price.

# Training
- Trained the model using:
     - **Optimizer:** Adam
     - **Loss Function:** Mean Squared Error
     - **Batch Size:** 32
     - **Epochs:** 30

# Model Evaluation
- **Auto ARIMA:** Evaluated using Mean Absolute Error (MAE) and visual inspection.
- **LSTM:** Evaluated using Mean Squared Error (MSE) and plot comparisons.

# Results
- Auto ARIMA provided accurate forecasts with confidence intervals.
- LSTM captured non-linear patterns and provided robust future price predictions.

# Tools and Libraries
- Python
- **Libraries:**
     - pandas
     - numpy
     - matplotlib
     - seaborn
     - tensorflow/keras
     - sklearn
     - statsmodels
     - pmdarima
