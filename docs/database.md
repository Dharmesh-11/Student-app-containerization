# 🗄️ MariaDB Setup & Configuration Guide

This guide explains how to install MariaDB, secure it, create a database, and configure a user.

---

## 🚀 1. Install MariaDB (Ubuntu)
```
sudo apt update
sudo apt install mariadb-server -y
```
---

## 🔐 2. Secure MariaDB Installation

Run the following command:
```
mysql_secure_installation
```
### Follow the prompts to:
- Set root password
- Remove anonymous users
- Disable remote root login
- Remove test database

---

## 🧑‍💻 3. Login to MariaDB
```
mysql -u root -p
```
Enter your root password when prompted.

---

## 🗃️ 4. Create Database & User

### Create Database
```
CREATE DATABASE student_db;
```

### Grant Privileges
```
GRANT ALL PRIVILEGES ON student_db.* TO 'username'@'localhost' IDENTIFIED BY 'your_password';
```
FLUSH PRIVILEGES;

> Replace `username` and `your_password` with your desired credentials.

---

## 🔑 5. Database Credentials (For Backend)

You will need the following details:

- DB_HOST = localhost
- DB_USER = username
- DB_PASS = your_password
- DB_PORT = 3306
- DB_NAME = student_db

---

## 📊 6. Create Table
```
USE student_db;

CREATE TABLE `students` (
  `id` bigint(20) NOT NULL AUTO_INCREMENT,
  `name` varchar(255) DEFAULT NULL,
  `email` varchar(255) DEFAULT NULL,
  `course` varchar(255) DEFAULT NULL,
  `student_class` varchar(255) DEFAULT NULL,
  `percentage` double DEFAULT NULL,
  `branch` varchar(255) DEFAULT NULL,
  `mobile_number` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=80 DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;
```
---

## ❌ Exit Database
```
EXIT;
```
---

## 🧠 Troubleshooting

| Issue | Solution |
|------|---------|
| Can't login | Check root password |
| Access denied | Verify user privileges |
| DB not found | Run CREATE DATABASE again |

---

## 🎯 Summary

- Install MariaDB
- Secure installation
- Create DB & user
- Create table
- Connect with backend
