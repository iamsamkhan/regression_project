Business Context
This case requires trainees to develop a model for predicting fraudulent transactions for afinancial
company and use insights from the model to develop an actionable plan. Data for thecase is available
in CSV format having 6362620 rows and 10 columns. Candidates can use whatever method they
wish to develop their machine learning model. Following usual model development procedures, the
model would be estimated on the calibration data and tested on the validation data. This case
requires both statistical analysis and creativity/judgment. We recommend you spend time on both
fine-tuning and interpreting the results of your machine learning model.
Data Dictionary & Source Acquisition
ffData Dictionary: The data dictionary of the dataset can be found here.
ffData Source: The dataset can be found here.
Your task is to execute the process for proactive detection of fraud while answering following
questions.
1. Data cleaning including missing values, outliers and multi-collinearity.
2. Describe your fraud detection model in elaboration.
3. How did you select variables to be included in the model?
4. Demonstrate the performance of the model by using best set of tools.
5. What are the key factors that predict fraudulent customer?
6. Do these factors make sense? If yes, How? If not, How not?
7. What kind of prevention should be adopted while company update its infrastructure?
8. Assuming these actions have been implemented, how would you determine if they work?
To begin, I would start by analyzing the data to understand the distribution of the target variable
(fraud or non-fraud) and the relationship between the variables. I would also check for any missing
values, outliers, or other issues that need to be addressed in the data cleaning phase.
Once the data is cleaned, I would then split the data into a training and validation set to build and
evaluate the model. I would use various machine learning algorithms like Random Forest, Logistic
Regression, and Neural Network to train the model. I would use techniques like cross-validation
and grid search to fine-tune the model and select the best performing model.
After selecting the best model, I would evaluate its performance using metrics such as accuracy,
precision, recall, F1-score, and AUC-ROC. I would also use techniques like feature importance and
partial dependence plots to understand which features are most important in predicting fraud.

With the insights gained from the model, I would develop an actionable plan for the financial company to proactively detect and prevent fraud. This plan could include implementing monitoring and
detection systems, training employees to recognize and report suspicious activity, and developing
strategies for identifying and mitigating high-risk transactions.
Finally, to determine if the actions taken to prevent fraud are working, I would track the number
of fraudulent transactions over time, as well as the financial losses caused by fraud. I would also
monitor the performance of the fraud detection model over time to ensure it continues to be effective.
HERE I AM USING KAGGLE ONLINE NOTEBOOK AS THE JUPITER NOTEBOOK USING ANACONDA WAS NOT COMPATIABLE
Data cleaning: Before building a model, it is important to clean the data. This includes handling missing values, identifying and handling outliers, and checking for multi-collinearity among
variables. Missing values can be handled by either dropping rows with missing values or imputing
them with a method such as mean or median imputation. Outliers can be identified by visualizing
the data or using statistical methods such as the Z-score. Multi-collinearity can be checked by
calculating the correlation matrix and identifying variables with high correlation.
Fraud detection model: The specific model used for fraud detection can vary depending on the
data and the problem at hand. Some common models used for fraud detection include logistic
regression, decision trees, and neural networks. I would use Random Forest Classifier, which is an
ensemble method that combines multiple decision trees to make a prediction. Random Forest is
a powerful algorithm, which can handle high-dimensional data with a large number of variables
and can also handle categorical variables. It can also be used for feature selection, which is an
important step in identifying the most relevant variables for predicting fraud.
Variable selection: Variables can be selected using different methods such as correlation analysis,
mutual information, or recursive feature elimination. I would use feature importance provided by
Random Forest Classifier to select top variables.
Model performance: Model performance can be evaluated using metrics such as accuracy, precision, recall, F1-score, and AUC-ROC. I would use confusion matrix, classification report, ROC-AUC
curve and precision-recall curve to evaluate model performance.
Key factors predicting fraudulent customer: The key factors that predict fraudulent customers can be identified by interpreting the model’s coefficients or feature importances. These
factors may include demographic information, transaction history, and other relevant variables.
Factors making sense: The factors that predict fraudulent customers should make sense in the
context of the problem and the data. For example, if the model is identifying customers with a
history of suspicious transactions as more likely to be fraudulent, that makes sense in the context
of fraud detection.
Prevention: To prevent fraud, the company can implement measures such as monitoring transactions for unusual patterns, implementing fraud detection software, and training employees to
recognize and report suspicious activity.
Evaluating actions: To determine if the actions taken to prevent fraud are working, the company
can track the number of fraudulent transactions over time, as well as the financial losses caused by
fraud. Additionally, the company can use metrics such as precision, recall, and F1-score to evaluate
the performance of the fraud detection model over time.
1. Data cleaning including missing values, outliers and multi-collinearity.
Data cleaning is an important step in preparing the data for modeling. It ensures that
the data is accurate, consistent, and ready for analysis. The following are some steps
that can be taken for data cleaning in this case:
1. Missing values: Missing values can cause issues with the model and its performance.
To handle missing values, I would first check the percentage of missing values in
each column, and if it is not too high, I would impute the missing values with the
mean, median, or mode of the column. If the percentage of missing values is high,
I would consider dropping that column.
2. Outliers: Outliers can also cause issues with the model and its performance. To
handle outliers, I would use techniques such as box plots, histograms, and scatter
plots to identify and visualize the outliers. Once identified, I would either remove
the outliers or replace them with the median or mean value.
3. Multi-collinearity: Multi-collinearity occurs when two or more variables are highly
correlated. This can cause issues with the model and its interpretation. To check
for multi-collinearity, I would calculate the correlation matrix for all the variables,
and if any variables are highly correlated, I would remove one of them or combine
them into a new variable.
2. Describe your fraud detection model in elaboration
To develop a model for detecting fraudulent transactions, I would use a supervised
machine learning approach. The dataset provided has labeled data, where a transaction
is labeled as “fraud” or “non-fraud”. This allows us to train a model to predict the class
label of a new transaction as “fraud” or “non-fraud”.
There are different types of supervised machine learning algorithms that can be used for
this task, such as decision trees, random forests, logistic regression, and neural networks.
However, for this problem, I would use an algorithm called Random Forest.
Random Forest is an ensemble algorithm that creates multiple decision trees and combines them to make predictions. It works by randomly selecting a subset of the data to
train each decision tree. This process is repeated multiple times, and the predictions of
all the trees are combined to make a final prediction.
One of the advantages of using Random Forest is that it can handle high dimensional
data and it’s less prone to overfitting. Random Forest also provides feature importance which can be used to identify the most important features that are driving the
predictions.
To train the model, I would first split the data into a training set and a testing set,
with 80% of the data used for training and 20% of the data used for testing. I would
then use the training set to train the Random Forest model and use the testing set to
evaluate the performance of the model.
20
To evaluate the performance of the model, I would use metrics such as accuracy, precision, recall, F1-score, and AUC-ROC. These metrics give an overall idea of how well
the model is performing, and they help to identify any areas where the model might
need improvement.
Once the model is trained and its performance is evaluated, it can be used to make
predictions on new transactions, with the aim of identifying fraudulent transactions
before they occur.
3. How did you select variables to be included in the model?
Selecting the appropriate variables to be included in the model is an important step
in the model development process. The following are some steps that I would take to
select the variables for the model:
1. Correlation analysis: I would start by calculating the correlation matrix for all
the variables in the dataset. This would give me an idea of which variables are
highly correlated with the target variable (fraud/non-fraud) and which variables
are highly correlated with each other. I would then select the variables that are
highly correlated with the target variable and have low correlation with other
variables.
2. Feature importance: I would use the feature importance provided by Random Forest algorithm to select the most important features that are driving the predictions.
Random Forest algorithm gives an importance score to each feature based on how
much they contribute to the predictions. The features with higher importance
scores would be selected for the model.
3. Domain Knowledge: I would also take into account any prior knowledge or domain
knowledge that I have about the data and the problem. For example, if I know
that certain features, such as transaction amount and location, are important in
identifying fraudulent transactions, I would make sure to include those in the
model.
4. Data visualization: I would also use visualization techniques such as box plots,
histograms, and scatter plots to identify patterns and trends in the data. This
would help me identify any variables that are important for the model but may
not be obvious from the correlation matrix or feature importance scores.
4. Demonstrate the performance of the model by using best set of tools.
To demonstrate the performance of the model, I would use several evaluation metrics
and visualization tools. These would include:
1. Confusion Matrix: A confusion matrix is a table that is used to define the performance of a classification model. It gives a summary of the true positives, true
negatives, false positives, and false negatives. The matrix can be used to calculate
other metrics such as accuracy, precision, recall, and F1-score.
2. ROC Curve and AUC: Receiver Operating Characteristic (ROC) curve is a graphical representation of the performance of a classification model at all classification
thresholds. The area under the ROC curve (AUC) is a measure of how well the
21
model can distinguish between positive and negative classes. A model with a higher
AUC is considered to be a better model.
3. Precision-Recall Curve: Precision-Recall curve is a plot of the precision (positive
predictive value) versus the recall (sensitivity) for different threshold settings. The
precision-recall curve is useful when the proportion of positive instances in the
dataset is low.
4. Feature Importance: As mentioned before, Random Forest algorithm gives an
importance score to each feature based on how much they contribute to the predictions. This can be used to identify the most important features in the model
and how they contribute to the model’s predictions.
5. Lift Chart: a lift chart is a visualization of the performance of a model when
compared to random guessing. It is a plot of the cumulative gains in true positive
rate (TPR) against the cumulative gains in false positive rate (FPR) for different
thresholds.
5. What are the key factors that predict fraudulent customer?
The key factors that predict fraudulent customers would depend on the specific dataset
and the features included in the model. However, some common factors that are often
used in fraud detection models include:
1. Demographic information: This includes information such as age, gender, income,
occupation, etc. which can be used to identify patterns in fraudulent behavior
among certain groups of people.
2. Transaction information: This includes information such as the amount of the
transaction, the location of the transaction, the time of the transaction, etc. which
can be used to identify patterns in fraudulent behavior among certain types of
transactions.
3. Behavioral information: This includes information such as the number of transactions, the frequency of transactions, the types of products/services purchased, etc.
which can be used to identify patterns in fraudulent behavior among certain types
of customers.
4. IP address: IP address can be used to identify the location of the transaction and
also to identify patterns in fraudulent behavior among certain geographic regions.
5. Device information: This includes information such as the type of device used for
the transaction, the browser used, the operating system used, etc. which can be
used to identify patterns in fraudulent behavior among certain types of devices.
6. Email address: Email address can be used to identify patterns in fraudulent behavior among certain types of email addresses.
6. Do these factors make sense? If yes, How? If not, How not?
These factors make sense as they are commonly used in fraud detection models and are
known to be associated with fraudulent behavior. For example:
1. Demographic information: People from different age groups, genders, income levels, and occupations may have different patterns of fraudulent behavior. For exam22
ple, older individuals may be less likely to engage in fraudulent activities compared
to younger individuals.
2. Transaction information: Fraudulent transactions often have certain characteristics such as large transaction amounts, transactions taking place in unfamiliar
locations, or transactions taking place at unusual times. By analyzing this information, patterns of fraudulent behavior can be identified.
3. Behavioral information: Fraudulent customers often have different patterns of behavior compared to legitimate customers. For example, they may make a large
number of transactions in a short period of time, or they may purchase high-risk
products/services.
4. IP address: A single IP address can be associated with multiple fraudulent activities, and by analyzing the location of the IP address fraudulent activities can be
identified.
5. Device information: Fraudulent activities can be associated with certain types of
devices such as mobile devices, or certain operating systems or browsers.
6. Email address: Certain types of email address are often associated with fraudulent
activities. For example, disposable email addresses or temporary email addresses
are often used for fraudulent activities.
7. What kind of prevention should be adopted while company update its infrastructure?
There are several prevention measures that a financial company can adopt to protect
against fraudulent transactions while updating its infrastructure. Some of these include:
1. Implementing multi-factor authentication: This can include using a combination
of something the user knows (like a password), something the user has (like a
phone or security token), and something the user is (like a fingerprint or facial
recognition).
2. Implementing transaction monitoring and anomaly detection: This can include
using machine learning algorithms to identify patterns of fraudulent behavior and
flagging suspicious transactions for further investigation.
3. Implementing fraud detection software: This can include using software that can
detect and prevent fraud in real-time, such as anti-fraud platforms that use machine
learning algorithms to identify patterns of fraudulent behavior.
4. Implementing security protocols: This can include implementing security protocols
such as encryption and secure socket layer (SSL) certificates to protect customer
data and transactions.
5. Employee training: Employee training on how to identify and prevent fraud can
be very beneficial in preventing fraudulent activities.
6. Implementing fraud prevention best practices: This can include implementing best
practices such as the Payment Card Industry Data Security Standard (PCI DSS)
or the Financial Services - Information Sharing and Analysis Center (FS-ISAC)
best practices.
23
7. Continuously monitoring: Continuously monitoring transactions for unusual activity, and keeping an eye out for new types of fraud that may emerge.
8. Regularly updating anti-fraud software: Regularly updating anti-fraud software to
keep up with new types of fraud and keep customer data secure.
8. Assuming these actions have been implemented, how would you determine if they
work?
To determine if the implemented fraud prevention measures are effective, the company
should regularly monitor and evaluate the performance of the measures. Some methods
of evaluating the effectiveness of the fraud prevention measures include:
1. Measurement of fraud rate: The company should track the rate of fraudulent
transactions before and after the implementation of the fraud prevention measures,
and compare the rates to determine if there has been an improvement.
2. False positive rate: It’s important to track the rate of false positives, as these can
cause inconvenience to legitimate customers and can lead to loss of trust.
3. Measurement of detection rate: The company should track the rate of successful fraud detections before and after the implementation of the fraud prevention
measures, and compare the rates to determine if there has been an improvement.
4. Measurement of response time: The company should track the time it takes to
detect and respond to fraudulent transactions before and after the implementation
of the fraud prevention measures, and compare the times to determine if there has
been an improvement.
5. Customer feedback: The company should gather feedback from customers about
their experiences with the fraud prevention measures, and use this feedback to
identify areas for improvement.
6. Audit and compliance: The company should regularly perform internal and external audits to ensure that the implemented fraud prevention measures are in
compliance with industry regulations and best practices.
