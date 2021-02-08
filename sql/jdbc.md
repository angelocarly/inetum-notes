# JDBC
Set of Java classes for interacting with a specific database.  
Three types of drivers:
- JDBC-native API Driver
- JDBC-net Driver
- JDBC Driver

## Connection Object
Used to communicate with the database

## Statement
Used to perform queries through the Connection object

## ResultSet
Results of a Statement

## Typical flow
1. Load the JDBC driver and create a database connection
2. Create a Statement and execute the query to get a ResultSet
3. Traverse and process the ResultSet
4. Close the ResultSet, Statement and Connection

# Connection to MySQL Using JDBC Driver

