# 🚀 Full Stack Student Management System

This project is a full-stack application built using:

- 🌐 Frontend: React (Vite)
- ⚙️ Backend: Spring Boot
- 🗄️ Database: MariaDB

---

# 📚 Project Documentation

Detailed guides for each layer:

- 🌐 [Frontend Setup Guide](docs/frontend.md)
- ⚙️ [Backend Deployment Guide](docs/backend.md)
- 🗄️ [Database Configuration Guide](docs/database.md)

---

# 📦 Prerequisites

Ensure the following are installed:

- Node.js & npm
- Java (JDK 17+)
- Maven
- MariaDB

---

# 🏗️ Architecture Overview

Frontend → Backend → Database

---

# 🚀 Quick Deployment Steps

## 1️⃣ Setup Database

- Install MariaDB
- Create database & user
- Create tables

## 2️⃣ Start Backend

- Configure `application.properties`
- Build using Maven
- Run JAR file

## 3️⃣ Setup Frontend

- Install dependencies
- Configure `.env`
- Build project

## 4️⃣ Deploy Frontend

- Install Apache
- Copy `dist/` files
- Access via browser

---

# 🌍 Application Access

- Frontend: http://<SERVER_IP>
- Backend API: http://<SERVER_IP>:8080

---

# 📁 Project Structure

project-root/
│
├── frontend/
├── backend/
├── docs/
│   ├── frontend.md
│   ├── backend.md
│   ├── database.md
│
└── README.md

---

# 🧠 Troubleshooting

| Issue | Solution |
|------|---------|
| Backend not starting | Check Java & Maven |
| DB connection error | Verify credentials |
| Frontend not loading | Check Apache |
| API not working | Verify `.env` |

---

# 🎯 Tech Stack

- React (Frontend)
- Spring Boot (Backend)
- MariaDB (Database)
- Apache (Deployment)

---

# 🚀 Future Enhancements

- Dockerize full application 🐳
- CI/CD pipeline ⚙️
- AWS Deployment ☁️
