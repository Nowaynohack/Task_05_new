Task 5: Role-Based Access Control (RBAC) in MySQL
🎯 Objective
Implement SQL-level access control for different user roles (Admin, Editor, Viewer) using MySQL roles, users, and privileges.

🛠 Tools
MySQL 8+ (supports CREATE ROLE, GRANT, REVOKE)
📂 Deliverables
SQL user creation script
Privileges list per role
Role usage demo (screenshots)
⚙️ Setup Instructions
Open MySQL and run the provided rbac.sql script.
This script will:
Create a database CompanyDB
Create sample tables: Employees, Projects
Create roles: AdminRole, EditorRole, ViewerRole
Assign privileges to each role
Create users and assign them roles
🔑 Roles & Privileges
Role	Privileges (on CompanyDB.*)	Use Case
Admin	ALL PRIVILEGES (Full access: SELECT, INSERT, UPDATE, DELETE, CREATE, DROP, ALTER)	Database Administrator
Editor	SELECT, INSERT, UPDATE	Data entry & updates, no delete
Viewer	SELECT (Read-only)	Reporting, analysis
👤 User Accounts
Username	Password	Role
admin_user	Admin@123	AdminRole
editor_user	Editor@123	EditorRole
viewer_user	Viewer@123	ViewerRole
▶️ Demo Usage
1. Login as Viewer
-- Allowed
SELECT * FROM Employees;

-- Not Allowed
INSERT INTO Employees (Name, Department, Salary) VALUES ('Amit', 'HR', 45000);


