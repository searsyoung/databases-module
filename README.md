## Submission

> What data types do each of these values represent?
- "A Clockwork Orange"

A. string
- 42

A. integer
- 09/02/1945

A. date
- 98.7

A. float
- $15.99

A. decimal

> Explain when a database would be used. Explain when a text file would be used.

A. Database - whenever you need to CRUD data that will be accessed from multiple endpoints, and/or if you have large amounts of data that would be unweildy to manage in a text file. 

Text files - are useful if you have a simple application that doesn't need to be accessed from multiple locations where file locking won't be a concern. Also useful if you want to limit complexity and you don't have to do a lot of complex data retrieval (which could become a perf bottleneck).


> Describe one difference between SQL and other programming languages.

A. SQL is a declarative programming language, meaning you request the data you're looking for, and the database does all the work to find it for you. Other languages are procedural, meaning you have define all of the steps that you want taken for the given data retrieval/manipulation task.  

> In your own words, explain how the pieces of a database system fit together at a high level.

A. Somewhere, a database host is made accessible to your application. This host stores data in a binary format, exposing access through an endpoint with the data in table format. Each table is constructed of columns and rows, containing various types of data. When you need to retrieve or manipulate the data, the application calls the endpoint with the request, which the database handles/resolves, and returns back a status (or result) to the application. 

> Explain the meaning of table, row, column, and value.

A. Table is the database structure for storing the data. A row is a record. A column is the type of data that will be stored within that cell of the table. The value is the actual piece of data being stored in the row:cell. 

> List three data types that can be used in a table.

A. Integer, string, float. 

> Given this payments table, provide an English description of the following queries and include their results:

     SELECT date, amount
     FROM payments;
    
    A. Show me the date and amount for all records in the payment table.

     SELECT amount
     FROM payments
     WHERE amount > 500;
    
    A. Show me the amount for all records in the payments table where the amount is greater than 500.

     SELECT *
     FROM payments
     WHERE payee = 'Mega Foods';

     A. Show me all columns from the payments table for any payee with the exact match of 'Mega Foods'


> Given this users table, write SQL queries using the following criteria and include the output:


>> The email and sign-up date for the user named DeAndre Data.

A. 

    SELECT email, signup
    FROM users
    WHERE payee = 'DeAndre Data';


| email        | signup           | 
| :-------------: |:-------------:|
| datad@comcast.net     | 2008-01-20 |


>> The user ID for the user with email 'aleesia.algorithm@uw.edu'.

A. 

    SELECT userid
    FROM users
    WHERE email = 'aleesia.algorithm@uw.edu';


| userid        |
| :-------------: |
| 1     | 

>> All the columns for the user ID equal to 4.

A. 

    SELECT *
    FROM users
    WHERE userid = 4;

| userid        | name     | email | signup |
| :-------------: |:-------------:|:-------------:|:-------------:|
|   4   | Brandy Boolean | bboolean@nasa.gov| 1999-10-15|