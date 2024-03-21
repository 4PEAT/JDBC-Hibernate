

#### Question 1: What does JDBC stand for?
- **Answer: B) Java Database Connectivity**

#### Question 2: Which of the following is used to establish a connection with the database?
- **Answer: A) DriverManager**

#### Question 3: Which interface is used to execute SQL queries and return the results?
- **Answer: B) Statement**

#### Question 4: In JDBC, what represents an SQL statement that you execute against the database?
- **Answer: C) Statement**

#### Question 5: Which method is used to start a transaction in JDBC?
- **Answer: C) setAutoCommit(false)**

#### Question 6: How can you retrieve data from a ResultSet?
- **Answer: B) By calling next() method followed by getXXX() methods**

#### Question 7: What does the executeUpdate() method return?
- **Answer: B) The number of rows affected by the query**

#### Question 8: Which of the following is true about PreparedStatement?
- **Answer: C) It is used for executing precompiled SQL statements multiple times efficiently.**

#### Question 9: What does the setAutoCommit(boolean autoCommit) method do?
- **Answer: B) It allows manual control over transaction commits.**

#### Question 10: Which method is used to manually commit changes made during a transaction?
- **Answer: A) commit()**

#### Question 1: What does ORM stand for, in the context of Hibernate?
- **Answer: B) Object-Relational Mapping**

#### Question 2: Which of the following is the core interface of Hibernate?
- **Answer: B) Session**

#### Question 3: What is the purpose of the @Entity annotation?
- **Answer: B) To mark a class as a persistent Java class**

#### Question 4: What does the SessionFactory interface do?
- **Answer: C) Creates sessions and stores configuration information**

#### Question 5: Which of the following is true about the first-level cache in Hibernate?
- **Answer: C) It is associated with the Session object**

#### Question 6: Which method is used to make an object persistent in Hibernate?
- **Answer: D) Both A and B are correct**
   - Both `save()` and `persist()` methods are used to make an object persistent.

#### Question 7: What is the HQL?
- **Answer: A) Hibernate Query Language**

#### Question 8: How can you achieve lazy loading for a collection in Hibernate?
- **Answer: C) By setting fetch type to LAZY**
   - Lazy loading is achieved by setting the fetch type of a collection to LAZY, not by default behavior or the @LazyCollection annotation.

#### Question 9: Which of the following is NOT a valid fetching strategy in Hibernate?
- **Answer: D) insert**
   - "insert" is not a fetching strategy; valid fetching strategies include select, join, and subselect.

#### Question 10: What is the purpose of the @GeneratedValue annotation?
- **Answer: C) To generate values for the primary key using the specified strategy**
   - The @GeneratedValue annotation specifies the generation strategy for the primary key values.
