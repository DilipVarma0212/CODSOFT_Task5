# CODSOFT_TASK3

Project Summary: This is the task of the  Build a model to identify fraudulent credit card transactions. Preprocess and normalize the transaction data, handle class imbalance issues, and split the dataset into training and testing sets. Train a classification algorithm, such as logistic regression or random forests, to classify transactions as fraudulent or genuine.Evaluate the model's performance using metrics like precision, recall, and F1-score, and consider techniques like oversampling or undersampling for improving results.


TOOL USED: SQL Server Management Studio (Transact-SQL)


CREATE TABLE creditcard command is as follow:
 
	  CREATE TABLE creditcard 
	  (
	      Time INT,
	      V1 FLOAT,
	      V2 FLOAT,
	      V3 FLOAT,
	      V4 FLOAT,
	      V5 FLOAT,
	      V6 FLOAT,
	      V7 FLOAT,
	      V8 FLOAT,
	      V9 FLOAT,
	      V10 FLOAT,
	      V11 FLOAT,
	      V12 FLOAT,
	      V13 FLOAT,
	      V14 FLOAT,
	      V15 FLOAT,
	      V16 FLOAT,
	      V17 FLOAT,
	      V18 FLOAT,
	      V19 FLOAT,
	      V20 FLOAT,
	      V21 FLOAT,
	      V22 FLOAT,
	      V23 FLOAT,
	      V24 FLOAT,
	      V25 FLOAT,
	      V26 FLOAT,
	      V27 FLOAT,
	      V28 FLOAT,
	      Amount FLOAT,
	      Class INT
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
	


