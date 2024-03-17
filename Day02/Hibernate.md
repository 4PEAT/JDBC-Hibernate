
### Library Management System

**Objective:** Develop a Java application using Hibernate ORM to manage books and authors in a library system. The application should demonstrate the use of `@Entity`, `@Table`, `@Column`, `@SecondaryTable`, and `@MappedSuperclass` annotations for mapping Java objects to database tables.

#### Requirements:

1. **Setup Environment:**
   - Set up a Java project with Hibernate.
   - Configure Hibernate with a MySQL or H2 database.

2. **Database Schema:**
   - Two main tables: `authors` and `books`.
   - The `books` table should have a secondary table `book_details` for storing detailed information.

3. **Entity Design:**
   - Create a `Person` class as a `@MappedSuperclass` that includes common attributes such as `id`, `firstName`, and `lastName`.
   - Extend `Person` class to create an `Author` entity. The `Author` entity should be mapped to the `authors` table.
   - Create a `Book` entity with attributes like `id`, `title`, and `ISBN`. It should be mapped to the `books` table and use a secondary table `book_details` to store details like `publisher` and `publicationYear`.

#### Steps:

1. **Implement the `Person` Class:**
   - Annotate the class with `@MappedSuperclass`.
   - Include common attributes and annotate them with `@Column` where necessary.

2. **Implement the `Author` Entity:**
   - Annotate the class with `@Entity` and `@Table(name = "authors")`.
   - Extend the `Person` class.
   - Implement relationships if needed, for example, to books.

3. **Implement the `Book` Entity:**
   - Annotate the class with `@Entity` and `@Table(name = "books")`.
   - Use `@SecondaryTable(name = "book_details")` to define a secondary table.
   - Map attributes to columns in both tables using `@Column`, specifying the `table` attribute for fields in the secondary table.

4. **Hibernate Configuration:**
   - Configure Hibernate to connect to your database.
   - Ensure that your entities are included in the Hibernate configuration.

5. **Testing:**
   - Implement a simple CRUD (Create, Read, Update, Delete) operation for both `Author` and `Book` entities.
   - Test the application to ensure that entities are correctly persisted to and retrieved from the database.

