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


-- Insert the provided data into the table
INSERT INTO credit_card_transactions 
(Time, V1, V2, V3, V4, V5, V6, V7, V8, V9, V10, V11, V12, V13, V14, V15, V16, V17, V18, V19, V20, V21, V22, V23, V24, V25, V26, V27, V28, Amount, Class)
VALUES
		(0, -1.359807134, -0.072781173, 2.536346738, 1.378155224, -0.33832077, 0.462387778, 0.239598554, 0.098697901, 0.36378697, 0.090794172, -0.551599533, -0.617800856, -0.991389847, -0.311169354, 1.468176972, -0.470400525, 0.207971242, 0.02579058, 0.40399296, 0.251412098, -0.018306778, 0.277837576, -0.11047391, 0.066928075, 0.128539358, -0.189114844, 0.133558377, -0.021053053, 149.62, 0),
		(1, 1.191857111, 0.266150712, 0.166480113, 0.448154078, 0.060017649, -0.082360809, -0.078802983, 0.085101655, -0.255425128, -0.166974414, 1.612726661, 1.065235311, 0.489095016, -0.143772296, 0.635558093, 0.463917041, -0.114804663, -0.18336127, -0.145783041, -0.069083135, -0.225775248, -0.638671953, 0.101288021, -0.339846476, 0.167170404, 0.125894532, -0.008983099, 0.014724169, 2.69, 0),
		(2, -1.358354062, -1.340163075, 1.773209343, 0.379779593, -0.503198133, 1.800499381, 0.791460956, 0.247675787, -1.514654323, 0.207642865, 0.624501459, 0.066083685, 0.717292731, -0.165945923, 2.345864949, -2.890083194, 1.109969379, -0.121359313, -2.261857095, 0.524979725, 0.247998153, 0.771679402, 0.909412262, -0.689280956, -0.327641834, -0.139096572, -0.055352794, -0.059751841, 378.66, 0),
		(3, -0.966271712, -0.185226008, 1.79299334, -0.863291275, -0.01030888, 1.247203168, 0.23760894, 0.377435875, -1.387024063, -0.054951922, -0.226487264, 0.178228226, 0.50775687, -0.287923745, -0.631418118, -1.059647245, -0.684092786, 1.965775003, -1.23262197, -0.208037781, -0.108300452, 0.005273597, -0.190320519, -1.175575332, 0.647376035, -0.221928844, 0.062722849, 0.061457629, 123.5, 0),
		(4, -1.158233093, 0.877736755, 1.548717847, 0.403033934, -0.407193377, 0.095921462, 0.592940745, -0.270532677, 0.817739308, 0.753074432, -0.822842878, 0.53819555, 1.345851593, -1.119669835, 0.17512113, -0.451449183, -0.237033239, -0.038194787, 0.803486925, 0.40854236, -0.009430697, 0.798278495, -0.13745808, 0.141266984, -0.206009588, 0.502292224, 0.21942223, 0.215153147, 69.99, 0),
		(5, -0.425965884, 0.960523045, 1.141109342, -0.16825208, 0.420986881, -0.029727552, 0.476200949, 0.260314333, -0.568671376, -0.371407197, 1.34126198, 0.359893837, -0.358090653, -0.1371337, 0.517616807, 0.401725896, -0.058132823, 0.068653149, -0.033193788, 0.084967672, -0.208253515, -0.559824796, -0.026397668, -0.371426583, -0.232793817, 0.105914779,

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
	


