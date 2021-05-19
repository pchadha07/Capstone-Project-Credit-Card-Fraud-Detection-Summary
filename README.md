# Capstone-Project-Credit-Card-Fraud-Detection-Summary
Problem statement is to identify/tag the fraudulent transactions using a classifier model and therefore help in cost saving for the bank in terms number of calls made to verify the transactions.
Dataset: Dataset contains around 0.2 million transactions made by customers; each transaction has customer level details and transaction time and amount along with the fraud prediction indicator. Data is, expectedly, unbalanced with only 500 class ‘1’s or fraudulent transactions and rest valid transactions.
Approach:
Data Understanding:  Go through the given data set and understand the importance of features provided. There are 28 numerical columns, with PCA al ready performed on them to preserve privacy of data. Two columns are in original state, the transaction amount and time between subsequent transactions. The ‘time’ feature could be dropped but will take final call after confirming that an important feature cannot be derived from same.
Data cleaning: Check for any null values or outliers in the data set given and correct them. There are no null values in the columns.
Feature selection: Analyze the variables using respective analysis such as univariate or bi-variate plots, correlation plots and pick the right set of features.
Scaling: Scaling is not needed in this case as the features provided are principal components and therefore have gaussian distribution however we must check for the skewness of data.
Model Building:
Treating class imbalances: Since there is class imbalance in the data (only 0.172 percent of transactions are fraud) will use SMOTE, ADASYN techniques to boost the number of fraud transactions. These two techniques are preferred as they will add more information points as well rather than just multiplying the existing data points
Model Selection: We will use different classifier algorithms (Logistic regression, Random Forest, Xgboost) and chose the one that best fits the model give the evaluation metrics and model complexity and computational needs. Will use GridSearch and K-fold cross validation for automated model tuning and validation process
Regularization and hyper parameter tuning: We will try out different combinations of hyper parameters to get best performing model. Also use regularization techniques in case of overfitting
Model evaluation: We will use evaluation metrics like precision, recall, ROC-AUC, accuracy to choose the model best predict the test data. Only ‘Accuracy’ will not suffice here as the data is highly imbalanced and so model could still show high accuracy, even though may not predict fraudulent transactions correctly, which is off most importance here.

Performing cost benefit analysis:
After selection of best model, will calculate the cost savings that would result from accurate model classification.
