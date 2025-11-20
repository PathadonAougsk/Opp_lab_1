Overview
This project is based / Heavy rely on OOP principle.

Psudo Overview..?
-> load csv file
-> extract to dictionary
-> filter / aggregate the data in dictionary

Starting from the top.

Class: DataLoader
This class is all about handling CSV file loading and converting it into a list containing dictionaries.
Each dictionary represents a row of data, making it easier to process programmatically.

Class: DB
This class functions as a lightweight storage system for multiple tables.
Different methods:
  - insert(self, table):
  insert a table into db list
  - search(self, userkey):
  find table with name {userkey} and return the table

Class: Table
This class represents the data table itself.
It contain methods to:
  - Filter(lamda) rows based on a given condition
  - Aggregate(key : str, condtion : lamda) specific columns using custom functions (like average, max, or count).
  - Join(self, initTable, tablekey) Joinning params table with the object table that has been call
  Return A new table combining two table

The idea is to should make it easier to code/edit by following OOP principles such as encapsulation and reusability.

How to test and run your code
Place the CSV files in the same directory as the script, then run:
"python data_processing.py"

Check outputs printed in the console to verify:
  - CSV loading
  - Filtering results
  - Join results
  - Aggregate calculations
This confirms each class works as expected.
