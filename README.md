# **Task 1: Prediction using Supervised ML**

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


# **Task 2: Prediction using Unsupervised ML**

**Task Overview:**

- The task involved predicting the optimum number of clusters from the given 'Iris' dataset and representing the results visually.

**Process:**

**Data Acquisition:**

Dataset URL:

- The dataset was provided at the URL https://bit.ly/3kXTdox.

Description:

- The dataset contains measurements of iris flowers from three different species: Iris-setosa, Iris-versicolor, and Iris-virginica. The features include SepalLengthCm, SepalWidthCm, PetalLengthCm, and PetalWidthCm.

**Data Exploration and Visualization:**

**Loading the Data:**

- The dataset was loaded into a pandas DataFrame.
- The first few rows of the dataset were displayed to understand its structure.

**Summary Statistics:**

- Summary statistics were generated to gain insights into the data distribution, including mean, standard deviation, minimum, maximum, and quartiles.

**Missing Values:**

- The dataset was checked for any missing values, and it was confirmed that there were no missing values.

**Visualizing Relationships:**

- Pair plots were created using seaborn to visualize the relationships between the different features and to see how the different species are distributed in the feature space.
- The pair plots indicated that Iris-setosa is clearly separable from the other two species, while Iris-versicolor and Iris-virginica show some overlap.

**Data Preparation:**

**Dropping Unnecessary Columns:**

- The 'Id' and 'Species' columns were dropped from the dataset as they are not needed for clustering.

**Standardizing the Data:**

- The data was standardized using StandardScaler to ensure that each feature contributes equally to the clustering process.

**Model Training:**

**Optimum Number of Clusters:**

- The optimum number of clusters was determined using the Elbow method. This involves running the K-means algorithm for a range of cluster numbers (from 1 to 100) and plotting the within-cluster sum of squares (inertia) for each number of clusters.
- The Elbow graph indicated that the optimum number of clusters is 3, as the rate of decrease in within-cluster sum of squares slows down after this point.

**Training the K-means Model:**

- The K-means model was trained with the optimal number of clusters (3) using the standardized data.
- The K-means algorithm assigned each data point to one of the three clusters.

**Model Prediction:**

**Cluster Assignment:**

- The model's cluster assignments were added to the original dataset as a new column named 'Cluster'.

**Model Evaluation:**

**Elbow Graph:**

- The Elbow graph was plotted to visualize the within-cluster sum of squares for different numbers of clusters, helping to determine the optimal number of clusters.

**Cluster Visualization:**

- Scatter plots were created to visualize the clustering results. These plots showed the clusters in terms of the original species and the clusters found by the K-means algorithm.
- The first two principal components were used for visualization to provide a clear view of the cluster separation.

**Model Used:**

**K-means Clustering:**

- The K-means clustering algorithm was used to identify the optimal number of clusters and assign each data point to a cluster. K-means is suitable for this task as it effectively partitions the data into distinct groups based on feature similarity.

**Results:**

**Data Visualization:**

**Pair Plots:**

- Pair plots indicated clear separability of Iris-setosa from the other two species, with some overlap between Iris-versicolor and Iris-virginica.

**Elbow Graph:**

**Optimal Number of Clusters:**

- The Elbow graph showed a significant bend at 3 clusters, indicating that 3 is the optimal number of clusters for this dataset.

**Cluster Visualization:**

**Cluster Scatter Plots:**

- Scatter plots showed the clusters formed by the K-means algorithm. These plots confirmed that the algorithm effectively grouped similar data points together.


# **Task 6: Prediction using Decision Tree Algorithm**

**Task Overview:**

The objective of this task was to create a Decision Tree classifier to predict the class of iris flowers based on their features and to visualize the classifier graphically. The purpose was to develop a model that can correctly classify new data and provide an interpretable decision-making process.

**Process:**

**Data Acquisition:**

Dataset URL: 

- The dataset was provided at the URL https://bit.ly/3kXTdox.

Description: 

- The dataset contains measurements of iris flowers from three species: Iris-setosa, Iris-versicolor, and Iris-virginica. Features include SepalLengthCm, SepalWidthCm, PetalLengthCm, and PetalWidthCm.

**Data Exploration and Visualization:**

**Loading the Data:**

- The dataset was loaded into a pandas DataFrame.
- The first few rows of the dataset were displayed to understand its structure.

**Summary Statistics:**

- Summary statistics provided insights into the data distribution.

**Missing Values:**

- The dataset was checked for any missing values, confirming there were none.

**Visualizing Relationships:**

- Pair plots were created using seaborn to visualize the relationships between features:
- Iris-setosa was clearly separable from the other two species.
- Iris-versicolor and Iris-virginica showed some overlap but could be partially separated by Petal Length and Petal Width.
- Distribution histograms were created for each feature.
- A correlation matrix heatmap was generated to visualize relationships between numerical features.

**Data Preparation:**

**Dropping Unnecessary Columns:**

- The 'Id' column was dropped as it was not needed for classification.

**Model Training:**

**Splitting the Data:**

- The data was split into features (X) and the target variable (y).
- The target variable 'Species' was encoded using LabelEncoder.
- The data was split into training and testing sets using a 70-30 split.

**Training the Decision Tree Model:**

- The Decision Tree classifier from the scikit-learn library was used.

**Model Prediction:**

**Making Predictions:**

- The trained model was used to predict the classes of the test data.

**Model Evaluation:**

**Performance Metrics:**

- Accuracy, Precision, Recall, and F1-Score were calculated to evaluate the model's performance.

- The confusion matrix and classification report provided a detailed evaluation of the model.

**Visualization of the Decision Tree:**

- The Decision Tree was visualized using plot_tree from the scikit-learn library, showing the structure and decision rules.

**Model Used:**

**Decision Tree Classifier:**

- The Decision Tree classifier was used to predict the class of iris flowers based on their features. This model is suitable for classification tasks and provides a clear, interpretable structure for decision making.

**Results:**

**Data Visualization:**

- Pair Plots and Histograms:

- Pair plots and histograms showed the clear separability of Iris-setosa from the other two species and some overlap between Iris-versicolor and Iris-virginica.

Heatmap:

- The correlation matrix heatmap provided insights into the relationships between numerical features.

**Model Performance:**

- Accuracy: 1.00

- Precision: 1.00

- Recall: 1.00

- F1-Score: 1.00

- These metrics indicated that the model achieved perfect accuracy on the test data, correctly classifying all instances.

**Confusion Matrix:**

- The confusion matrix showed that all instances were correctly classified, with no misclassification.

**Classification Report:**

- The classification report confirmed perfect precision, recall, and F1-scores for all classes.

**Decision Tree Visualization:**

- The Decision Tree was visualized, showing the structure of the classifier and the decision rules based on the features.
