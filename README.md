## Movie Rating Prediction

## Author: CHANDRAHAS K

## Batch: NOVEMBER

## Domain: Data Science

## Aim

The aim of this project is to build a model that predicts movie ratings based on given features.

## Datasets

The following datasets were used for this project:

1. movies.dat: Contains movie information after preprocessing, including MovieName, Genre, and MovieIDs.
2. ratings.dat: Contains ratings information after preprocessing, including Ratings and Timestamp.
3. Users.dat: Contains user information after preprocessing, including Gender, Age, Occupation, and Zip-code.

## Libraries Used

The following important libraries were used for this project:

- numpy
- pandas
- matplotlib.pyplot
- seaborn
- sklearn.preprocessing.LabelEncoder
- sklearn.preprocessing.MinMaxScaler
- sklearn.model_selection.train_test_split
- sklearn.linear_model.LogisticRegression
- chardet
- sklearn.metrics.accuracy_score
- sklearn.metrics.classification_report

## Data Exploration and Preprocessing

1. The Movie_data, Ratings_data, and Users_data were loaded as DataFrames from separate CSV files.
2. The missing values in each DataFrame were dropped using `dropna(inplace=True)`.
3. The shape and descriptive statistics for each DataFrame were displayed using `data.shape`,`data.info` and `data.describe()`.
4. The 'Gender' column in Users_data was encoded from categorical to numerical values using LabelEncoder.
5. The DataFrames were concatenated horizontally using `pd.concat` and`pd.merge` to create a final dataset `data`.
6. Unnecessary columns like 'Occupation', 'Zip-code', and 'Timestamp' were dropped from the final dataset to create `cleardata`.
7. Any remaining missing values in the final dataset `cleardata` were dropped using `dropna()`.
8. Data visualization was performed using count plots and histograms to gain insights into the distribution of ratings, genders, and age.

## Model Training

1. The feature matrix `input` and target vector `target` were created using relevant columns from the final dataset `cleardata`.
2. The data was split into training and testing sets using `train_test_split`.
3. The input data was scaled using MinMaxScaler to normalize the values between 0 and 1.

## Model Prediction

1. A logistic regression model was initialized and trained on the training data using `LogisticRegression`.
2. The model was used to predict movie ratings for the test set using `model.predict(X_test)`.

##Model Evaluation

In the provided code, {accuracy:.2f}, this is a formatted string in Python, often used to display numeric values with a specific number of decimal places. Let me break it down:
`{}:` This is a placeholder for the value to be inserted into the string.
`accuracy:` This is the variable or value that will replace the placeholder.
`:.2f:` This is a formatting option specifying how to display the value. In this case, it means to display the value as a floating-point number with 2 decimal places.
