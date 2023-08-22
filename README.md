DESCRIPTION

The sinking of the Titanic is one of the most infamous shipwrecks in history. On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew. While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others. In this challenge, we ask you to build a predictive model that answers the question: “What sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).

BUSINESS UNDERSTANDING

What is the goal of the project? What is the problem that you are trying to solve?

To predict what sorts of people were more likely to survive.

ANALYTIC APPROACH

What kind of analytics should we use? Predictive? Descriptive?

Because the goal of the project requires predicting True/False answers, we need to use the Classification model.

DATA REQUIREMENT

What kind of data is needed for the project?

In order to predict data, including both binary or specific values, we require labeled data. In this particular project, we need binary data.

DATA COLLECTION

Where are the data come from? How to gather the data?

The data was downloaded from Kaggle in CSV format. 

DATA UNDERSTANDING 

The data include 3 CSV files, which are gender_submission.csv, test.csv, and train.csv. Each file contains columns, ie:

train.csv: Should be used to build your machine-learning models. For the training set, we provide the outcome (also known as the “ground truth”) for each passenger. Your model will be based on “features” like passengers’ gender and class. You can also use feature engineering to create new features.

test.csv: Should be used to see how well your model performs on unseen data. For the test set, we do not provide the ground truth for each passenger. It is your job to predict these outcomes. For each passenger in the test set, use the model you trained to predict whether or not they survived the sinking of the Titanic.

gender_submission.csv: A set of predictions that assume all and only female passengers survive, as an example of what a submission file should look like.

variable notes:

pclass: A proxy for socio-economic status (SES)

1st = Upper

2nd = Middle

3rd = Lower

age: Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

sibsp: The dataset defines family relations in this way...

Sibling = brother, sister, stepbrother, stepsister

Spouse = husband, wife (mistresses and fiancés were ignored)

parch: The dataset defines family relations in this way...

Parent = mother, father

Child = daughter, son, stepdaughter, stepson. Some children traveled only with a nanny, therefore parch=0 for them.

DATA PREPARATION

- Clean data: Replace missing values with frequent values and mean values using NumPy.

- Transforming: Transform data type. Convert categorical values into numerical values using LabelEncoder.

- Standardizing: Transform data values into smaller values using StandardScaler.

MODELING

- Split data: Split 70% of the data for training and 30% of the data for testing purposes, with random_state parameter = 2.

- Model selection: Logistic Regression

- Model parameters selection: Use GridSearchCV to find the best parameter with the best score.

- Predict targeted value: Use the selected model to fit the training set and predict the test set.

EVALUATION

Use accuracy_score to find the score between the targeted value in the test set and the predicted value. 
