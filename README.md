# DATABASE-EMPLOYMENT-MANAGEMENT-SYSTEM
HOTEL DBM
EMPLOYMENT MANAGEMENT SYSTEM FOR HOTEL – DBMS PROJECT REPORT
1.EXECUTIVE SUMMARY
This project presents the design and implementation of an Employment Management System for a Hotel using a relational database approach. The system is developed to efficiently manage employee-related information such as departments, job roles, attendance, and payroll.
The primary goal of this system is to replace manual record-keeping with a structured database that ensures data accuracy, consistency, and quick retrieval. The system supports key operations such as storing employee details, tracking attendance, managing salaries, and generating reports.
Using MySQL within XAMPP, the system was implemented with properly normalized tables, relationships, and constraints to ensure data integrity. The project demonstrates how database systems can improve organizational efficiency, reduce redundancy, and support decision-making.
2.BUSINESS CASE
 Application Domain
The system is designed for the hotel management sector, specifically focusing on employee management. It supports the following operations:
Employee registration and record management
Department and job assignment
Attendance tracking
Payroll processing
Report generation
Users of the System
Hotel Managers
HR Personnel
Accountants
 Benefits of the System
Tangible Benefits
Reduced paperwork and storage costs
Faster data retrieval
Improved payroll accuracy
Reduced human errors
Intangible Benefits
Improved employee management
Better decision-making
Increased operational efficiency
Data security and integrity
 Cost Analysis
Tangible Costs
Computer systems
Software (XAMPP, MySQL)
Maintenance
Intangible Costs
Training staff
Time required for system adoption
 The benefits outweigh the costs, making the system economically viable.
 User Issues
Users may require training to use the system
Resistance to change from manual systems
Basic computer literacy is required
 Risk Assessment
Technical Risks
System failure
Data loss
Organizational Risks
Lack of user adoption
Poor data entry practices
Mitigation
Regular backups
User training
 Limitations
No web interface (console-based system)
Limited scalability for very large hotels
No real-time analytics
Does not handle advanced HR features
. SYSTEM DESIGN
3.1 Logical Design (E-R Modeling)
The database follows a relational model where data is segmented into specialized entities to minimize duplication.
Entities and Attributes
Department: dept_id (PK), dept_name
Job: job_id (PK), job_title, base_salary
Employee: emp_id (PK), f_name, l_name, gender, contact, dept_id (FK),job_id (FK)
Attendance: att_id (PK), emp_id (FK), date, check_in, status
Payroll: pay_id (PK), emp_id (FK), bonus, deductions, net_salary
 ER Diagram
()
 Physical Design
Database Schema
Department table
Job table
Employee table
Attendance table
Payroll table
All tables are linked using foreign keys to maintain referential integrity.
 User Interface
Command-line interface (MySQL Shell)
Queries used to insert, update, and retrieve data
 IMPLEMENTATION
 System Setup
Software: XAMPP (MySQL)
Language: SQL
Platform: Windows
 Screenshots;  
“DOUBLE CLICK IN THE SHCREENSHOTS BELOW TO VIEW ALL THE 6 SCREENSHOTS”
DOUBLE CLICK IN THE ABOVE SCREENSHOTS TO SEE ALL THE 6 SCREENSHOTS
 Table Creation
Example:
CREATE TABLE Department (
    department_id INT AUTO_INCREMENT PRIMARY KEY,
    department_name VARCHAR(50)
);
 Sample Data Inserted
Departments: Reception, Kitchen, Management
Employees: John, Mary, David, Sarah
Attendance records
Payroll details
 Queries and Results
Query 1: View Employees
SELECT * FROM Employee;
Query 2: Employees with Departments
SELECT e.first_name, d.department_name
FROM Employee e
JOIN Department d ON e.department_id = d.department_id;
Query 3: Payroll Report
SELECT employee_id, net_salary FROM Payroll

Results
Data stored successfully
Relationships enforced
Queries returned correct outputs
 BIBLIOGRAPHY
Database System Concepts 
MySQL Documentation
Lecture Notes
Online tutorials and references

CONCLUSION
The Employment Management System successfully demonstrates how database systems can be used to manage employee data efficiently. By using structured tables, relationships, and SQL queries, the system ensures accuracy, consistency, and fast data retrieval.
The project highlights the importance of database design and shows how DBMS tools can solve real-world problems in organizations such as hotels.


