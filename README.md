**Task 1: Prediction using Supervised ML**

**Task Overview:**
- The task involved predicting the percentage score of a student based on the number of hours they studied using a simple linear regression model. This was a beginner-level task designed to introduce the basics of supervised machine learning.

**Process:**

**Data Acquisition:**

- The dataset was provided at the URL: http://bit.ly/w-data.
- The dataset contained two variables: Hours (number of study hours) and Scores (percentage scores).

**Data Exploration and Visualization:**

- The dataset was loaded into a pandas DataFrame.
- The first few rows of the dataset were displayed to understand its structure.
- Summary statistics were generated to gain insights into the data distribution.
- The dataset was checked for any missing values.
- The relationship between study hours and scores was visualized using a scatter plot.

**Data Preparation:**

- The dataset was separated into features (X) and target variable (y). In this case, Hours was the feature and Scores was the target variable.
- The data was split into training and testing sets using an 80-20 split.

**Model Training:**

- The Linear Regression model from the scikit-learn library was used.
- The model was trained using the training data (X_train and y_train).

**Model Prediction:**

- The trained model was used to predict scores on the testing data (X_test).
- The predicted scores were compared with the actual scores to evaluate the model's performance.

**Model Evaluation:**

- Evaluation metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE) were calculated to quantify the model's prediction error.
- These metrics helped in understanding the average error and the distribution of errors in the predictions.

**Specific Prediction:**

- The score for a student who studied for 9.25 hours/day was predicted using the trained model.
- The regression line was visualized along with the data points to illustrate the fit of the model.

**Model Used:**

**Linear Regression Model:**
- A simple linear regression model was used to predict the percentage score based on the number of study hours. Linear regression was suitable for this task as it involved predicting a continuous target variable using a single feature.

**Results:**

**Data Visualization:**

- A scatter plot showed the relationship between study hours and percentage scores.

**Model Performance:**

- Mean Absolute Error (MAE): 3.92

- Mean Squared Error (MSE): 18.94

- Root Mean Squared Error (RMSE): 4.35

- These metrics indicated that the model's predictions were reasonably close to the actual values, with an average prediction error of approximately 3.92 percentage points.

**Predicted Score for 9.25 Hours/Day:**

- The model predicted that a student who studied for 9.25 hours/day would score approximately 92.39%.

**Regression Line Visualization:**

- A plot showed the regression line along with the data points, highlighting the linear relationship between study hours and scores.
