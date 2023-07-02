#Sales Forecasting with Machine Learning
This repository contains a Python script for sales forecasting using machine learning algorithms. The script reads sales data from an Excel file, performs data preprocessing, trains different regression models, and generates sales predictions for each product.

##Introduction
The sales_forecasting.py script is designed to forecast future sales based on historical data. It uses various regression models, including Linear Regression and Random Forest Regression, to predict sales for the next 12 months. The script also includes data visualization to help understand the sales trends and the accuracy of the predictions.

##Challenge
Sales forecasting is crucial for businesses to plan their operations, optimize inventory management, and make informed decisions. However, accurately predicting future sales can be challenging due to the complex nature of sales data and the presence of various factors influencing sales patterns.

##Solution
The sales forecasting script tackles the challenge by leveraging machine learning techniques. It follows the following steps to generate sales predictions:

Reading Data: The script reads sales data from an Excel file (etsy_all_clean_skus.xlsx), which should be placed in the project directory.

Data Preprocessing: The script performs necessary data preprocessing steps, including filtering the data for each product, aggregating monthly sales, and calculating the sales differences between consecutive months.

Feature Engineering: The script transforms the monthly sales differences into a supervised learning problem by creating input features for the current month and using the next month's sales difference as the label.

Train-Test Split: The data is split into training and testing sets, where the training set contains the historical sales data, and the testing set contains the most recent 12 months of data.

Model Training: The script trains a Random Forest Regression model to predict the sales differences for the next month based on the previous 12 months of data.

Prediction and Evaluation: The trained model is used to predict the sales differences for the test data. The predictions are then transformed back to the sales values by adding them to the actual sales of the previous month. The Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R2) values are calculated to evaluate the model's performance.

Visualization: The script includes data visualization to compare the actual sales with the predicted sales for the test data.

Output: The predicted sales for each product are stored in a DataFrame (df_rest_of_year) and saved as CSV (June_predictions_2023.csv) and Excel (june_predictions_2023.xlsx) files.

##Usage
Clone or download this repository to your local machine.

Place the sales data file (etsy_all_clean_skus.xlsx) in the project directory.

Ensure that the required packages (pandas, numpy, matplotlib, xgboost, scikit-learn, tensorflow) are installed in your Python environment.

Open the sales_forecasting.py file in a Python IDE or text editor.

Run the script to generate sales forecasts for each product.

##Note
You can modify the script to explore different regression models or adjust the hyperparameters of the existing models for better accuracy.

The provided code is a basic implementation. You can enhance it further by adding more features, incorporating additional models, or integrating with other data sources.

Ensure that the sales data file (etsy_all_clean_skus.xlsx) is in the correct format and contains the required columns (sku, month_year, sales).



Acknowledgments
The script makes use of various machine learning libraries and techniques for sales forecasting, including scikit-learn, XGBoost, and TensorFlow. The code is inspired by the need for accurate sales predictions and
