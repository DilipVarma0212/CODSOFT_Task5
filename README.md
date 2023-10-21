# CODSOFT_TASK3

Project Summary: This is the task of the  Build a model to identify fraudulent credit card transactions. Preprocess and normalize the transaction data, handle class imbalance issues, and split the dataset into training and testing sets. Train a classification algorithm, such as logistic regression or random forests, to classify transactions as fraudulent or genuine.Evaluate the model's performance using metrics like precision, recall, and F1-score, and consider techniques like oversampling or undersampling for improving results.


TOOL USED: SQL Server Management Studio (Transact-SQL)


CREATE TABLE creditcard command is as follow:
 
	  CREATE TABLE creditcard 
	  (
	      Time INT not null,
	      V1 FLOAT not null,
	      V2 FLOAT not null,
	      V3 FLOAT not null,
	      V4 FLOAT not null,
	      V5 FLOAT not null,
	      V6 FLOAT not null,
	      V7 FLOAT not null,
	      V8 FLOAT not null,
	      V9 FLOAT not null,
	      V10 FLOAT not null,
	      V11 FLOAT not null,
	      V12 FLOAT not null,
	      V13 FLOAT not null,
	      V14 FLOAT not null,
	      V15 FLOAT not null,
	      V16 FLOAT not null,
	      V17 FLOAT not null,
	      V18 FLOAT not null,
	      V19 FLOAT not null,
	      V20 FLOAT not null,
	      V21 FLOAT not null,
	      V22 FLOAT not null,
	      V23 FLOAT not null,
	      V24 FLOAT not null,
	      V25 FLOAT not null,
	      V26 FLOAT not null,
	      V27 FLOAT not null,
	      V28 FLOAT not null,
	      Amount FLOAT not null,
	      Class INT not null
	  )



Retrive all rows from table creditcard

	  SELECT * 
	  FROM creditcard


Retrive specific columns from table creditcard

	  SELECT Time, Amount, Class 
	  FROM creditcard
	  WHERE Class = 0


Count the total number of records from table creditcard

	  SELECT COUNT(*) AS total_records 
	  FROM creditcard


Count the number of fraudulent transactions from table creditcard

	  SELECT COUNT(*) AS fraudulent_transactions 
	  FROM creditcard 
	  WHERE Class = 1


Count the number of genuine transactions from table creditcard

	  SELECT COUNT(*) AS genuine_transactions 
	  FROM creditcard WHERE 
	  Class = 0


Calculate MEAN/AVERAGE of the Amount column from table credit

	  SELECT AVG(Amount) AS mean_amount
	  FROM creditcard


Calculate MINIMUM of the Amount column from table credit

	  SELECT MIN(Amount) AS min_amount
	  FROM creditcard


Calculate MAXIMUM of the Amount column from table credit

	  SELECT MAX(Amount) AS max_amount
	  FROM creditcard
	


