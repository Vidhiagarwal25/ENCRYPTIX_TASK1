# Titanic Survival Prediction

Batch: June Batch 2

Domain: Data Science


Problem Statement
Build a model that predicts whether a passenger on the Titanic survived or not. This is a classic beginner project with readily available data.


Dataset
The dataset for this project is imported from a CSV file, "Titanic-Dataset.csv". The dataset contains information about passengers on the Titanic, including their survival status, class (Pclass), sex (Gender), and age (Age).

Libraries Used
The following important libraries were used for this project:

-numpy <br>
-pandas <br>
-matplotlib.pyplot <br>
-seaborn <br>
-sklearn (.preprocessing.LabelEncoder, .model_selection.train_test_split, .linear_model.LogisticRegression)


Data Exploration and Preprocessing
1. The dataset was loaded using pandas as a DataFrame, and its shape and a glimpse of the first 5 rows were displayed using data.shape and data.head(5) and last 5 using data.tail(5).
2. Descriptive statistics for the numerical columns were displayed using data.describe() to get an overview of the data, including missing values.
3. The count of passengers who survived and those who did not was visualized using sns.countplot(x=data['Survived']).
4. The count of survivals was visualized with respect to the Pclass using sns.countplot(x=data['Survived'], hue=data['Pclass']).
5. The count of survivals was visualized with respect to the gender using sns.countplot(x=data['Sex'], hue=data['Survived']).
6. The survival rate by gender was calculated and displayed using df.groupby('Sex')[['Survived']].mean().
7. The 'Sex' column was converted from categorical to numerical values using LabelEncoder from sklearn.preprocessing.


Model Training:
1. The feature matrix X and target vector Y were created using relevant columns from the DataFrame.
2. The dataset was split into training and testing sets using train_test_split from sklearn.model_selection.
3. A logistic regression model was initialized and trained on the training data using LogisticRegression from sklearn.linear_model.


Model Prediction:
1. The model was used to predict the survival status of passengers in the test set.
2. The predicted results were printed using log.predict(X_test).
3. The actual target values in the test set were printed using Y_test.
4. A sample prediction was made using log.predict([[2, 1]]) with Pclass=2 and Sex=Male (1).
