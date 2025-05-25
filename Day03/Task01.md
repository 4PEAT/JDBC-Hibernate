

# **Task: Employee Management System with Hibernate**

## **Objectives**

* Implement a simple employee management system.
* Use Hibernate (via JPA) for managing the persistence layer.
* Apply **bidirectional** relationships using proper JPA annotations.
* Perform CRUD (Create, Read, Update, Delete) operations.
* Utilize join columns and join tables to map entity relationships.

---

## **Entities**

### **Department**

* `id` (Primary Key)
* `name` (String)
* `employees` (List of Employee)

**Relationship:**
✅ **Bidirectional One-to-Many**
A department can have many employees, and each employee references its department.

---

### **Employee**

* `id` (Primary Key)
* `name` (String)
* `position` (String)
* `department` (Department)
* `projects` (List of Project)

**Relationships:**
✅ **Many-to-One with Department**
✅ **Bidirectional Many-to-Many with Project**

---

### **Project**

* `id` (Primary Key)
* `title` (String)
* `employees` (List of Employee)

**Relationship:**
✅ **Bidirectional Many-to-Many**
Each project can have multiple employees, and each employee can be part of multiple projects.

---

## **Tasks**

### ✅ Configure the Persistence Environment

* Create a `persistence.xml` configuration file with the database connection details.
* Use the `DepartmentManagement` persistence unit.
* Recommended DB: H2 (in-memory) for simplicity and quick testing.

---

### ✅ Define the Entity Classes

* Annotate all entities with `@Entity`.
* Use:

  * `@Id` and `@GeneratedValue` for primary keys.
  * `@OneToMany` and `@ManyToOne` for Department ↔ Employee.
  * `@ManyToMany` with `@JoinTable` for Employee ↔ Project.

---

### ✅ Implement the DAO Layer

Create separate DAO classes for each entity:

* `DepartmentDAO`

  * `createDepartment(Department department)`

* `EmployeeDAO`

  * `createEmployee(Employee employee)`
  * `updateEmployee(Employee employee)`
  * *(Optional: add `deleteEmployee()` and `findEmployeeById()`)*

* `ProjectDAO`

  * `createProject(Project project)`

Each DAO should use `EntityManager` and `EntityTransaction` with proper transaction handling (`try-catch-finally`).

---

### ✅ Demonstrate Functionality in `Main.java`

* Create:

  * Two departments (e.g., IT and HR)
  * Two projects (e.g., Project A and Project B)
  * Two employees assigned to departments
* Assign employees to projects
* Persist all entities using DAO methods
* Update employees to reflect project assignments
* (Optional) Fetch and print department and project details

---

### ✅ Bonus Features

* Use **lazy loading** for collections (default in JPA).
* Show transaction management across multiple operations.
* Add `delete` and `read` functionality to the DAO layer.

---

## **Deliverables**

* **Entities:** `Department`, `Employee`, `Project` with correct annotations.
* **DAO Layer:** DAO classes with methods for CRUD operations.
* **Main Class:** Demonstrates entity creation, relationship mapping, and persistence.


