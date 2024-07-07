### Task: Select all departments

#### Solution:

```java
// Method to get all departments
public List<Department> getAllDepartments() {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Department> query = em.createQuery("from Department", Department.class);
        return query.getResultList();
    } finally {
        em.close();
    }
}
```

### Task: Select all employees

#### Solution:

```java
// Method to get all employees
public List<Employee> getAllEmployees() {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Employee> query = em.createQuery("from Employee", Employee.class);
        return query.getResultList();
    } finally {
        em.close();
    }
}
```

### Task: Select all projects

#### Solution:

```java
// Method to get all projects
public List<Project> getAllProjects() {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Project> query = em.createQuery("from Project", Project.class);
        return query.getResultList();
    } finally {
        em.close();
    }
}
```

### Task: Select a department by its ID

#### Solution:

```java
// Method to get a department by ID
public Department getDepartmentById(Long departmentId) {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Department> query = em.createQuery("from Department d where d.id = :id", Department.class);
        query.setParameter("id", departmentId);
        return query.getSingleResult();
    } finally {
        em.close();
    }
}
```

### Task: Select employees by department ID

#### Solution:

```java
// Method to get employees by department ID
public List<Employee> getEmployeesByDepartment(Long departmentId) {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Employee> query = em.createQuery(
                "select e from Employee e where e.department.id = :departmentId", Employee.class);
        query.setParameter("departmentId", departmentId);
        return query.getResultList();
    } finally {
        em.close();
    }
}
```

### Task: Select projects by employee ID

#### Solution:

```java
// Method to get projects by employee ID
public List<Project> getProjectsByEmployee(Long employeeId) {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Project> query = em.createQuery(
                "select p from Project p join p.employees e where e.id = :employeeId", Project.class);
        query.setParameter("employeeId", employeeId);
        return query.getResultList();
    } finally {
        em.close();
    }
}
```

### Task: Select employees along with their projects

#### Solution:

```java
// Method to get employees with their projects
public List<Employee> getEmployeesWithProjects() {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Employee> query = em.createQuery(
                "select distinct e from Employee e left join fetch e.projects", Employee.class);
        return query.getResultList();
    } finally {
        em.close();
    }
}
```

### Task: Select departments along with their employees

#### Solution:

```java
// Method to get departments with their employees
public List<Department> getDepartmentsWithEmployees() {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Department> query = em.createQuery(
                "select distinct d from Department d left join fetch d.employees", Department.class);
        return query.getResultList();
    } finally {
        em.close();
    }
}
```

### Task: Select projects along with their employees

#### Solution:

```java
// Method to get projects with their employees
public List<Project> getProjectsWithEmployees() {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Project> query = em.createQuery(
                "select distinct p from Project p left join fetch p.employees", Project.class);
        return query.getResultList();
    } finally {
        em.close();
    }
}
```

### Task: Count the number of projects for each employee

#### Solution:

```java
// Method to count the number of projects for each employee
public List<Object[]> getProjectCountByEmployee() {
    EntityManager em = emf.createEntityManager();
    try {
        TypedQuery<Object[]> query = em.createQuery(
                "select e.name, count(p) from Employee e join e.projects p group by e.name", Object[].class);
        return query.getResultList();
    } finally {
        em.close();
    }
}
```

### Task: Update the position of employees in a specific department

#### Solution:

```java
// Method to update the position of employees in a specific department
public void updateEmployeePositionByDepartment(Long departmentId, String newPosition) {
    EntityManager em = emf.createEntityManager();
    EntityTransaction tx = em.getTransaction();
    try {
        tx.begin();
        Query query = em.createQuery(
                "update Employee e set e.position = :newPosition where e.department.id = :departmentId");
        query.setParameter("newPosition", newPosition);
        query.setParameter("departmentId", departmentId);
        query.executeUpdate();
        tx.commit();
    } catch (Exception e) {
        if (tx.isActive()) {
            tx.rollback();
        }
        e.printStackTrace();
    } finally {
        em.close();
    }
}
```

### Task: Set department_id to null for all employees in a department

#### Solution:

```java
// Method to set department_id to null for all employees in a department
public void clearDepartmentFromEmployees(Long departmentId) {
    EntityManager em = emf.createEntityManager();
    EntityTransaction tx = em.getTransaction();
    try {
        tx.begin();
        Query updateEmployees = em.createQuery(
                "update Employee e set e.department = null where e.department.id = :departmentId");
        updateEmployees.setParameter("departmentId", departmentId);
        updateEmployees.executeUpdate();
        tx.commit();
    } catch (Exception e) {
        if (tx.isActive()) {
            tx.rollback();
        }
        e.printStackTrace();
    } finally {
        em.close();
    }
}
```
_______________________________________________________________________________________________________________________

Sure, here's how you can use the methods in each DAO class to perform various operations.

### Example Usage of `DepartmentDAO` Methods

#### Get All Departments
```java
public class Main {
    public static void main(String[] args) {
        DepartmentDAO departmentDAO = new DepartmentDAO();
        List<Department> departments = departmentDAO.getAllDepartments();
        System.out.println("All Departments:");
        for (Department department : departments) {
            System.out.println("Department: " + department.getName());
        }
    }
}
```

#### Get Department by ID
```java
public class Main {
    public static void main(String[] args) {
        DepartmentDAO departmentDAO = new DepartmentDAO();
        Department department = departmentDAO.getDepartmentById(1L);
        System.out.println("Department: " + department.getName());
    }
}
```

### Example Usage of `EmployeeDAO` Methods

#### Get All Employees
```java
public class Main {
    public static void main(String[] args) {
        EmployeeDAO employeeDAO = new EmployeeDAO();
        List<Employee> employees = employeeDAO.getAllEmployees();
        System.out.println("All Employees:");
        for (Employee employee : employees) {
            System.out.println("Employee: " + employee.getName());
        }
    }
}
```

#### Get Employees by Department ID
```java
public class Main {
    public static void main(String[] args) {
        EmployeeDAO employeeDAO = new EmployeeDAO();
        List<Employee> employees = employeeDAO.getEmployeesByDepartment(1L);
        System.out.println("Employees in Department 1:");
        for (Employee employee : employees) {
            System.out.println("Employee: " + employee.getName());
        }
    }
}
```

#### Get Employees with Projects
```java
public class Main {
    public static void main(String[] args) {
        EmployeeDAO employeeDAO = new EmployeeDAO();
        List<Employee> employees = employeeDAO.getEmployeesWithProjects();
        System.out.println("Employees with Projects:");
        for (Employee employee : employees) {
            System.out.println("Employee: " + employee.getName() + ", Projects: " + employee.getProjects().size());
        }
    }
}
```

#### Get Project Count by Employee
```java
public class Main {
    public static void main(String[] args) {
        EmployeeDAO employeeDAO = new EmployeeDAO();
        List<Object[]> projectCounts = employeeDAO.getProjectCountByEmployee();
        System.out.println("Number of Projects per Employee:");
        for (Object[] result : projectCounts) {
            System.out.println("Employee: " + result[0] + ", Projects: " + result[1]);
        }
    }
}
```

#### Update Employee Position by Department
```java
public class Main {
    public static void main(String[] args) {
        EmployeeDAO employeeDAO = new EmployeeDAO();
        employeeDAO.updateEmployeePositionByDepartment(1L, "Senior Developer");
        System.out.println("Updated positions for employees in Department 1.");
    }
}
```

#### Clear Department from Employees
```java
public class Main {
    public static void main(String[] args) {
        EmployeeDAO employeeDAO = new EmployeeDAO();
        employeeDAO.clearDepartmentFromEmployees(1L);
        System.out.println("Cleared department from employees in Department 1.");
    }
}
```

### Example Usage of `ProjectDAO` Methods

#### Get All Projects
```java
public class Main {
    public static void main(String[] args) {
        ProjectDAO projectDAO = new ProjectDAO();
        List<Project> projects = projectDAO.getAllProjects();
        System.out.println("All Projects:");
        for (Project project : projects) {
            System.out.println("Project: " + project.getTitle());
        }
    }
}
```

#### Get Projects with Employees
```java
public class Main {
    public static void main(String[] args) {
        ProjectDAO projectDAO = new ProjectDAO();
        List<Project> projects = projectDAO.getProjectsWithEmployees();
        System.out.println("Projects with Employees:");
        for (Project project : projects) {
            System.out.println("Project: " + project.getTitle() + ", Employees: " + project.getEmployees().size());
        }
    }
}
```
