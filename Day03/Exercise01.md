### Task: Employee Management System with Hibernate

#### Objectives:
- Implement a simple employee management system.
- Use Hibernate to manage the persistence layer.
- Understand and apply unidirectional and bidirectional relationships.
- Utilize join columns to connect entities.
- Perform CRUD operations.

#### Entities:
- `Department`: Represents departments within the company.
- `Employee`: Represents employees working in a department.
- `Project`: Represents projects that employees can be assigned to.

#### Relationships:
- A `Department` has a unidirectional one-to-many relationship with `Employee` (a department has many employees, but employees don't need to know their department).
- An `Employee` has a bidirectional many-to-many relationship with `Project` (employees can work on multiple projects, and projects can have multiple employees).

#### Tasks:

1. **Configure the Hibernate Environment**
   - Set up the Hibernate configuration file with the database details.
   - Define the H2 in-memory database for simplicity.

2. **Define the Entities with Annotations**
   - Create `Department`, `Employee`, and `Project` entities with proper Hibernate annotations.
   - Use `@OneToMany` for the unidirectional relationship between `Department` and `Employee`.
   - Use `@ManyToMany` with `@JoinTable` for the bidirectional relationship between `Employee` and `Project`.

3. **Implement CRUD Operations**
   - Write methods to perform the following operations:
     - **Create (C):** Add new departments, employees, and projects.
     - **Read (R):** Retrieve and display a list of all departments with their employees, and a list of all projects with their assigned employees.
     - **Update (U):** Change an employee’s department, update project details, and manage employee-project assignments.
     - **Delete (D):** Remove an employee, a department, or a project.

4. **Testing Your Setup**
   - Create a main class or integration tests to demonstrate the CRUD operations.
   - Test the unidirectional relationship by adding employees to a department and then retrieving the department’s employees.
   - Test the bidirectional relationship by assigning employees to projects, and then retrieving both the employees for a project and the projects for an employee.

5. **Bonus Challenges**
   - Implement lazy loading for the `Department` to `Employee` relationship and demonstrate how it works.
   - Add transaction management to handle operations that require multiple steps and may need to be rolled back.

6. **Deliverables**
   - Source code for all entities with annotations.
   - Source code for the service layer containing the CRUD operations.
   - Main class or tests showcasing the operations and results.
