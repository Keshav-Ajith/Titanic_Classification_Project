# Titanic_Classification_Project
## Summer Class final project

Using this notebook, we are able to find the the likelihood of a passenger on the titanic surviving using various machine learning models such as logistic regression, decision trees and random forest.

The Titanic dataset which is used for this project is loaded directly from a public URL using the pandas library. This dataset contains information about the passengers, including their demographics, ticket information, and survival status.

However, before actually starting making the model, this dataset had to be preprocessed:
  * Some columns in the dataset such as 'PassengerId', 'Name', 'Ticket', and 'Cabin' are dropped
  * Missing values in the 'Age' column are filled with the median age
  * The 'Sex' column is converted into numerical representation (0 for female, 1 for male) and renamed to the 'Gender' column
  * The 'Embarked' column, which is categorical, is changed to create separate binary columns for each embarkation point
  * The data is then split into features (X) and the target variable (y), which is 'Survived'
  * The data is then divided into training and testing sets to evaluate the models

The training data is used to trauin these models:
  * Logistic Regression: Logistic regression is a supervised machine learning algorithm primarily used for binary classification problems, where the goal is to predict the probability of a data point belonging to one of two categories.
  * Decision Trees: A decision tree classifier is a supervised machine learning algorithm used primarily for classification tasks. It models decisions and their possible consequences in a hierarchical, tree-like structure, similar to a flowchart.
  * Random Forest: A random forest classifier is an ensemble machine learning algorithm specifically designed for classification tasks. It operates by constructing a "forest" of multiple decision trees during training and outputting the class that is the mode of the classes predicted by individual trees.

Each model is initialized with a 'random_state' for reproducibility and then trained using the 'fit' method on the training data.

The trained models are evaluated on the test set to assess their performance. The primary evaluation metric used is **Accuracy**, which measures the proportion of correctly predicted instances. The accuracy score is calculated for each model using the 'accuracy_score' function.

The accuracy scores of the three models are compared to determine which model performed best in predicting Titanic passenger survival. The model with the highest accuracy is both logistic regression and random forest which both scored a percentage of 81.01%. The decision tree classifier only scored 78.77%.
