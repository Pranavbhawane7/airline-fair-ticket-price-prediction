##Airline Fare Ticket Price Prediction

---

##Introduction
This project predicts airline ticket fares using machine learning. By analyzing flight details such as airline, source, destination, departure/arrival times, and duration, the model learns pricing patterns and provides accurate predictions.

The notebook prediction.ipynb contains the complete workflow: data preprocessing, exploratory data analysis (EDA), feature engineering, model building, evaluation, and saving the trained model.

---

##Dataset
Features included:

Airline

Source and Destination

Date of Journey

Departure and Arrival times

Duration

Price

Preprocessing steps:

Dropped irrelevant columns (e.g., Route)

Handled missing values

Encoded categorical variables

Extracted new features (day, month, etc.)

---

##Workflow
Data Preprocessing

Cleaned dataset, handled missing values, dropped irrelevant columns.

Applied encoding to categorical variables.

Extracted new features from date/time columns.

Exploratory Data Analysis

Distribution plots showed skewness in ticket prices.

Boxplots revealed outliers (above ₹40,000).

Outliers handled using the Interquartile Range (IQR) method.

Correlation analysis identified key features influencing price.

Model Building

Models applied: Linear Regression, Decision Tree, Random Forest.

Hyperparameter tuning with RandomizedSearchCV.

Best model: RandomForestRegressor with parameters:

n_estimators=760

max_depth=30

min_samples_split=15

max_features='sqrt'

Evaluation

Metrics used: MAPE, MAE, RMSE, R².

Random Forest achieved the best performance with ~12–15% average error.

Feature importance: Airline, Duration, and Source/Destination were the most influential.

Model Saving

Final trained model saved using pickle for reuse.

---

##Results
Random Forest achieved the best predictive accuracy among tested models.

Average error (MAPE) ~12–15%.

Airline, Duration, and Source/Destination were the most important features.

Outliers were successfully handled using the IQR method.

---

##Conclusion
The project demonstrates how machine learning can be applied to predict airline ticket fares. With proper preprocessing, feature engineering, and hyperparameter tuning, Random Forest provided strong predictive accuracy. 
