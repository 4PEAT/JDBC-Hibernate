
### Task: Implement an Enhanced Library Management System using Hibernate

**Objective:** Develop a Java application that manages a library system, utilizing Hibernate for ORM. The system should manage authors and books, demonstrating comprehensive CRUD operations (Create, Read, Update, Delete) on these entities. The application will highlight the use of inheritance, complex mappings, and secondary tables in Hibernate.

#### Requirements:

1. **Entities:**
   - Implement an abstract `Person` class as a `@MappedSuperclass`, containing common fields such as `id`, `firstName`, and `lastName`.
   - Extend the `Person` class to create an `Author` entity. The `Author` entity should include additional fields such as `email`.
   - Create a `Book` entity that includes fields like `title`, `genre`, `publisher`, and `publicationYear`. Use a `@SecondaryTable` to separate publication details (`publisher` and `publicationYear`) from the main book details.

2. **Database:**
   - Use MySQL as the database for storing the library system's data.
   - Design the schema to accommodate the entities mentioned, ensuring that the `Book` entity utilizes a secondary table for publication details.

3. **CRUD Operations:**
   - Implement CRUD operations for both `Author` and `Book` entities. This includes creating, retrieving, updating, and deleting instances of these entities in the database.
   - Demonstrate the CRUD operations in the main application flow, showcasing the handling of entity relationships and the use of Hibernate session and transaction management.

4. **Configuration and Session Management:**
   - Configure Hibernate to connect to the MySQL database, ensuring that entity scanning is properly set up to automatically detect and map the entities.
   - Utilize proper session and transaction management practices to ensure data integrity and handle any potential exceptions gracefully.

5. **Testing:**
   - Write a series of tests or a main application flow that demonstrates each CRUD operation on both `Author` and `Book` entities. This includes creating new authors and books, reading them from the database, updating their information, and finally deleting them.
   - Ensure that the application correctly handles relationships, such as an author having multiple books.

- A `hibernate.cfg.xml` configuration file set up for use with a MySQL database.
- A main class that demonstrates the CRUD operations on the `Author` and `Book` entities, showcasing the application's functionality.
- (Optional) Unit tests or integration tests that verify the application's behavior under various scenarios.

This task aims to solidify understanding of Hibernate's capabilities in managing complex entity relationships, inheritance, and advanced mapping strategies, as well as enhancing proficiency in performing CRUD operations within a Java application.
