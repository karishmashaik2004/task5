# ☁️ Task 5: Cloud Database Setup using AWS RDS (MySQL)

## ✅ Objective
To create and connect a managed database instance in AWS RDS, perform SQL operations, and understand Database-as-a-Service (DBaaS).

---

## 🛠 Tools Used
- AWS RDS (Free Tier)
- MySQL Workbench
- SQL Query Language

---

## 🚀 Steps Performed

### 1️⃣ Created RDS MySQL Instance
- Engine: MySQL 8.0
- DB Instance Class: db.t3.micro
- Public access: Enabled
- Backup retention: 7 Days

📸 Screenshot: RDS Instance  
➡️ `screenshots/rds-instance.png`

---

### 2️⃣ Configured Security Group
- Allowed MySQL port **3306**
- Source: My IP ✅

📸 Screenshot: Inbound Rules  
➡️ `screenshots/inbound-rules.png`

---

### 3️⃣ Connected using MySQL Workbench
- Host: RDS Endpoint
- User: admin
- Port: 3306

📸 Screenshot: Successful Connection  
➡️ `screenshots/workbench-connection.png`

---

### 4️⃣ Executed SQL Queries
```sql
CREATE DATABASE intern_demo;
USE intern_demo;

CREATE TABLE students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(50),
  domain VARCHAR(30),
  score INT
);

INSERT INTO students (name, domain, score)
VALUES ('Aarav', 'Cloud', 95), ('Diya', 'DevOps', 89);

SELECT * FROM students;
