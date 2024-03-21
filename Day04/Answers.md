
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
