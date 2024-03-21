
### JDBC Quiz

#### Question 1: What does JDBC stand for?
A) Java Database Connection
B) Java Database Connectivity
C) Java Direct Connectivity
D) Java Data Control

#### Question 2: Which of the following is used to establish a connection with the database?
A) DriverManager
B) Connection
C) Statement
D) ResultSet

#### Question 3: Which interface is used to execute SQL queries and return the results?
A) Connection
B) Statement
C) ResultSet
D) DriverManager

#### Question 4: In JDBC, what represents an SQL statement that you execute against the database?
A) JDBCStatement
B) SQLQuery
C) Statement
D) QueryExecutor

#### Question 5: Which method is used to start a transaction in JDBC?
A) commit()
B) startTransaction()
C) setAutoCommit(false)
D) begin()

#### Question 6: How can you retrieve data from a ResultSet?
A) Using the get() method
B) By calling next() method followed by getXXX() methods
C) Direct access using column name
D) Through executeQuery() method

#### Question 7: What does the executeUpdate() method return?
A) A ResultSet object
B) The number of rows affected by the query
C) True or False depending on the execution success
D) Nothing, it returns void

#### Question 8: Which of the following is true about PreparedStatement?
A) It is slower than Statement because it is precompiled.
B) It cannot be used for SQL queries with parameters.
C) It is used for executing precompiled SQL statements multiple times efficiently.
D) It does not support batch updates.

#### Question 9: What does the setAutoCommit(boolean autoCommit) method do?
A) It automatically commits every SQL statement.
B) It allows manual control over transaction commits.
C) It disables the execution of SQL statements.
D) It automatically rolls back transactions if an error occurs.

#### Question 10: Which method is used to manually commit changes made during a transaction?
A) commit()
B) save()
C) persist()
D) flush()

Sure, here's a refreshed and detailed 10-question multiple-choice quiz on Hibernate, covering a range of topics from basic concepts to advanced features.

### Hibernate Multiple Choice Quiz

#### Question 1: What does ORM stand for, in the context of Hibernate?
A) Object-Related Mapping
B) Object-Relational Mapping
C) Object-Request Model
D) Option-Result Mapping

#### Question 2: Which of the following is the core interface of Hibernate?
A) JDBC
B) Session
C) Connection
D) Transaction

#### Question 3: What is the purpose of the @Entity annotation?
A) To create a new database table
B) To mark a class as a persistent Java class
C) To generate a primary key
D) To establish a connection to the database

#### Question 4: What does the SessionFactory interface do?
A) Creates new database sessions
B) Configures Hibernate for the application
C) Creates sessions and stores configuration information
D) Manages JDBC connections

#### Question 5: Which of the following is true about the first-level cache in Hibernate?
A) It is disabled by default.
B) It can be shared across sessions.
C) It is associated with the Session object.
D) It requires manual configuration.

#### Question 6: Which method is used to make an object persistent in Hibernate?
A) save()
B) persist()
C) commit()
D) Both A and B are correct

#### Question 7: What is the HQL?
A) Hibernate Query Language
B) High-Quality Language
C) Hibernate Quick Lookup
D) None of the above

#### Question 8: How can you achieve lazy loading for a collection in Hibernate?
A) By setting fetch type to EAGER
B) By using the @LazyCollection annotation
C) By setting fetch type to LAZY
D) Lazy loading is the default behavior for collections

#### Question 9: Which of the following is NOT a valid fetching strategy in Hibernate?
A) select
B) join
C) subselect
D) insert

#### Question 10: What is the purpose of the @GeneratedValue annotation?
A) To specify a custom generation strategy for primary keys
B) To automatically generate values for any field
C) To generate values for the primary key using the specified strategy
D) To validate the generated values before persisting
