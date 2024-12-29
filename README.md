# Employee Database Management System

## Overview
This project implements an **Employee Database Management System** using SQL scripts. It provides a structured database schema and operations to manage employee records effectively, including insertion, updates, deletions, and retrievals. The database is designed to store essential employee details such as ID, name, email, department, job position, salary, and hire date.

## Features
- **Database Creation**: Ensures the database is created only if it does not already exist.
- **Table Creation**: Employee table schema with constraints and default values.
- **Data Insertion**: Adds sample employee records.
- **Data Retrieval**: Queries to fetch employee data based on various conditions.
- **Data Manipulation**:
  - Updates employee information.
  - Deletes specific employee records.
- **Aggregation Queries**: Performs operations like counting employees, finding maximum/minimum salaries, and calculating averages.
- **Sorting and Filtering**: Provides ordered and filtered data retrieval.
- **Schema Modification**: Demonstrates table alteration by dropping a column.

## Technologies Used
- **Database**: MySQL / MariaDB (compatible with other SQL-based databases).
- **SQL**: Structured Query Language for database management.

## SQL Script
Refer to the file `employee_db_queries.sql` for the complete SQL script used to create and manage the database.

## Database Schema
```
EMPLOYEE(
    EMP_ID INT PRIMARY KEY,
    NAME VARCHAR(40) NOT NULL,
    EMAIL VARCHAR(40) NOT NULL,
    DEPT VARCHAR(20),
    JOB_POSITION VARCHAR(20) NOT NULL,
    SALARY DECIMAL(10,2) DEFAULT 30000.00,
    HIRED_DATE DATE NOT NULL DEFAULT CURRENT_DATE
)
```

## Setup Instructions
1. Ensure MySQL or MariaDB is installed on your system.
2. Open a MySQL client or command-line tool.
3. Execute the script file using the command:
   ```
   source employee_db_queries.sql;
   ```
4. Verify the database and table creation with:
   ```
   SHOW DATABASES;
   USE EMP;
   SHOW TABLES;
   ```
5. Test queries provided in the script to manage and analyze employee data.

## Usage Examples
1. Retrieve all employee records:
   ```sql
   SELECT * FROM EMPLOYEE;
   ```
2. Find employees with a salary greater than 55000:
   ```sql
   SELECT * FROM EMPLOYEE WHERE SALARY > 55000;
   ```
3. Count total employees:
   ```sql
   SELECT COUNT(*) FROM EMPLOYEE;
   ```

## Notes
- Ensure the database server is running before executing the script.
- Modify sample data and schema as per requirements.

## Contributing
Contributions are welcome! Feel free to fork this repository and submit pull requests.

## License
This project is licensed under the MIT License.

---
For any queries or suggestions, please contact [gaurirasal2919@gmail.com].
