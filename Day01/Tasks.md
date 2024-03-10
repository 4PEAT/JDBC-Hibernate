
### Task 1: Insert Multiple Records Using PreparedStatement
Modify the existing code to insert multiple records into the `Persons` table using a `PreparedStatement`. Ensure you use a loop or an array of person details to insert multiple records dynamically. This task helps you understand how to efficiently insert multiple rows into a database using JDBC.

### Task 2: Update a Record
Create functionality to update the address of a specific person in the `Persons` table. Use a `PreparedStatement` to perform this task by identifying the person with either their `PersonID` or `LastName`. This teaches you how to use parameters in JDBC to update records safely and prevents SQL injection attacks.

### Task 3: Delete a Record
Implement a method to delete a person from the `Persons` table based on a provided `PersonID` or `LastName`. Use `PreparedStatement` to execute the delete operation. This task will show you how to remove records from a database and the importance of using prepared statements for dynamic queries.

### Task 4: Implement Transaction Management
Modify the code to implement transaction management when inserting multiple records into the `Book` table. Ensure that if one insert fails, none of the records are persisted (use commit and rollback). This will help you understand transaction boundaries and how to manage database transactions in JDBC to ensure data integrity.

### Task 5: Call a Different Stored Procedure
Create a new stored procedure in your database, for example, `updatePersonLastName`, which updates the last name of a person based on their `PersonID`. Then, add code to call this procedure from your Java application. This task allows you to practice using `CallableStatement` for different types of database operations and understand how stored procedures can encapsulate business logic within the database.
