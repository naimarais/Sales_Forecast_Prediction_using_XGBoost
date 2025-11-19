# Sales_Forecast_Prediction_using_XGBoost

This project demonstrates building a sales forecasting model using Python and XGBoost.

Here's a summary of the steps involved:

Importing Libraries: Necessary libraries like pandas, matplotlib, seaborn, xgboost, and scikit-learn were imported.
Loading the Dataset: A sales dataset from 'train.csv' was loaded and the first few rows were displayed.
Data Preprocessing and Visualization: The 'Order Date' column was converted to datetime objects, and daily sales were aggregated. A line plot visualized the sales trend over time.
Feature Engineering - Creating Lagged Features: Lagged sales features were created to capture temporal patterns, using a lag of 5. Rows with missing values due to lagging were dropped.
Preparing Data for Training: The data was split into features (X) and target (y), and then further divided into training and testing sets (80% train, 20% test) while preserving chronological order.
Training the XGBoost Model: An XGBoost Regressor model was initialized and trained on the training data. The model was configured with objective='reg:squarederror', n_estimators=100, learning_rate=0.1, and max_depth=5.
Making Predictions and Evaluating the Model: Predictions were made on the test set, and the model's performance was evaluated using Root Mean Squared Error (RMSE). The RMSE was found to be 734.63, which was deemed acceptable given the scale of the sales data.
Visualizing Results: A plot comparing actual and predicted sales on the test set was generated, visually confirming the model's effectiveness in tracking sales trends.
The project concludes that sales forecasting using machine learning models like XGBoost can significantly enhance prediction accuracy by capturing temporal patterns, aiding businesses in optimizing inventory, pricing, and demand planning.
