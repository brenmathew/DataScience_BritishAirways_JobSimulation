# British Airways Data Science Job Simulation 

- Completed a simulation focussing on how data science is a critical component
   of British Airways success
- Scraped and analysed customer review data to uncover findings
- Built a predictive model to understand factors that influence buying
   behaviour

  # Data analysis:
Tasks done:
-Data Preprocessing:
-Data visualization
This code performs data cleaning on airline reviews, removing duplicates, special symbols, and extra spaces. 
It further uses the VADER sentiment analysis tool to analyze the sentiment of the reviews and visualizes the sentiment distribution using pie and bar charts. 
The final visualizations help in understanding the sentiment of the reviews in the dataset.

# Predictive Modelling:

- Mapping Categorical Features to Numeric Values:

1. Created a mapping dictionary string_to_int_mapping to map unique strings in the 'route' column to integers.
Use map() to replace the values in the 'route' column with the corresponding integer values.
Repeat the same process for the 'booking_origin' column.
One-Hot Encoding:

2. Defined a list categorical_columns containing the names of categorical columns ('flight_day', 'sales_channel', 'trip_type').
Use pd.get_dummies() to perform one-hot encoding on these categorical columns, creating binary columns for each category.
Split Data:

3. Split the data into features (X) and the target variable (y), where X contains all columns except 'booking_complete', and y contains 'booking_complete'.
Use train_test_split() to split the data into training and testing sets.
Machine Learning:

- Random Forest Classifier:

1. Initialized a Random Forest classifier (rf_classifier) with 100 estimators and a fixed random state for reproducibility (random_state=42).
Train the classifier on the training data using rf_classifier.fit().
Prediction and Evaluation:

2. Made predictions on the test data using rf_classifier.predict().
Calculate accuracy using accuracy_score() and print the result.
Feature Importance Visualization:

Feature Importance Analysis:

1. Get feature importances from the trained Random Forest classifier using rf_classifier.feature_importances_.
Create a DataFrame (feature_importance_df) to display feature names and their importance scores.
Sort the features by importance in descending order.
Plot Feature Importance:

2. Create a horizontal bar chart to visualize feature importance using plt.barh().
Invert the y-axis to display the most important features at the top.

In conclusion, This code prepares the data, trains a Random Forest classifier to predict customer bookings, analyzes feature importance, and visualizes key insights from the dataset,
such as preferred routes and average purchase lead time.
