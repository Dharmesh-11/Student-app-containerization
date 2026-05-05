# ⚙️ Backend Deployment Guide (Spring Boot)

This document provides step-by-step instructions to build and deploy a Spring Boot backend application.

---

## 🚀 Prerequisites

Ensure the following are installed:

- Java Development Kit (JDK 17 or higher)
- Maven
- Spring Boot project (source code or JAR)

---

## ☕ Step 1: Install Java

java -version

sudo apt update
sudo apt install openjdk-17-jdk -y

java -version

---

## 📦 Step 2: Install Maven

sudo apt install maven -y

mvn -version

---

## ⚙️ Step 3: Configure Database & Build Application

cd backend

vim src/main/resources/application.properties

server.port=8080
spring.datasource.url=jdbc:mariadb://<DB_HOST>:3306/<DB_NAME>
spring.datasource.username=<DB_USER>
spring.datasource.password=<DB_PASS>

---

## 🏗️ Build the Application

mvn clean package

---

## ▶️ Step 4: Run the Application

java -jar target/spring-backend-v1.jar

---

## 🌐 Access the Application

http://localhost:8080

---

## 🔄 Step 5: Run in Background

nohup java -jar target/spring-backend-v1.jar > app.log 2>&1 &

tail -f app.log
