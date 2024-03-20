**Task Description:**

You are tasked with developing a Java application to manage departments, employees, and projects using Hibernate for data persistence. The application should allow users to perform CRUD (Create, Read, Update, Delete) operations on departments, employees, and projects, as well as associate employees with departments and projects. Below are detailed requirements for each component:

1. **Department Management:**
   - Users should be able to create new departments by providing a unique name.
   - Existing departments can be updated, where users can modify the department's name.
   - Departments can be deleted from the system.

2. **Employee Management:**
   - Users should have the ability to add new employees, specifying their name, position, and the department they belong to.
   - Existing employee records can be updated, allowing users to modify the employee's name, position, or department association.
   - Employees can be removed from the system.

3. **Project Management:**
   - Users should be able to create new projects, providing a unique title for each project.
   - Existing projects can be updated, allowing users to modify the project's title.
   - Projects can be deleted from the system.

4. **Association Management:**
   - Employees can be associated with multiple projects, and projects can have multiple employees assigned to them.
   - Departments should have a collection of employees associated with them.

5. **Data Persistence:**
   - Use Hibernate for data persistence, configuring the database connection and mapping entities using annotations.
   - Ensure that data integrity is maintained during CRUD operations, and proper cascading behavior is defined for entity associations.

6. **Main Application:**
   - Implement a `Main` class to demonstrate the functionality of the application.
   - Use instances of DAO (Data Access Object) classes to interact with the database for CRUD operations.

7. **User Interface (Optional):**
   - Consider implementing a simple user interface, such as a command-line interface or a basic GUI, to facilitate interaction with the application.
   - The user interface should provide options for creating, updating, and deleting departments, employees, and projects.

8. **Testing and Documentation:**
   - Thoroughly test the application to ensure that all CRUD operations and entity associations work as expected.
   - Document the setup instructions for running the application, including any required dependencies or configuration steps.
   - Provide clear comments in the code to explain the functionality of each method and class, as well as any assumptions made during development.

9. **Submission:**
   - Submit the complete source code, including DAO classes, entity classes, configuration files, and any additional documentation required.
