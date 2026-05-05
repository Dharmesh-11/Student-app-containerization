# 🌐 Frontend Setup & Deployment Guide (React)

This document provides step-by-step instructions to set up, build, and deploy the React frontend application.

---

## 🚀 1. Prerequisites

Make sure the following tools are installed:

- Node.js
- npm (Node Package Manager)

### 📦 Install Node.js & npm (Linux)

sudo apt update
sudo apt install nodejs npm -y

### ✅ Verify Installation

node -v
npm -v

---

## 📥 2. Install Dependencies

Navigate to your project folder and run:

npm install

This installs all required packages from `package.json`.

---

## ⚙️ 3. Configure Environment Variables

Open the `.env` file:

vim .env

Update the backend API URL:

VITE_API_URL="http://<BACKEND_PUBLIC_IP>:8080/api"

> Replace `<BACKEND_PUBLIC_IP>` with your backend server IP address.

---

## 🏗️ 4. Build for Production

Run the following command:

npm run build

### 📁 Output

- A `dist/` folder will be generated
- Contains optimized production-ready files

---

## 🌐 5. Deploy Using Apache Server

### 📦 Install Apache

sudo apt install apache2 -y

### ▶️ Start Apache

sudo systemctl start apache2

### 📂 Copy Build Files

sudo cp -rf dist/* /var/www/html/

---

## 🌍 6. Access Application

Open your browser:

http://localhost:80

Or using server IP:

http://<YOUR_SERVER_IP>

---

## 📌 Important Notes

- Ensure port **80** is open (especially in AWS Security Groups)
- Backend server must be running
- Use HTTPS in production for better security

---

## 🧠 Troubleshooting

| Problem | Solution |
|--------|---------|
| App not loading | Check Apache status (`systemctl status apache2`) |
| API not working | Verify `.env` URL |
| Build failed | Run `npm install` again |

---

## 📁 Project Structure

project-root/
│
├── src/
├── public/
├── dist/        # Production build
├── package.json
├── .env
└── frontend.md

---

## 🎯 Summary

- Install dependencies → `npm install`
- Configure API → `.env`
- Build → `npm run build`
- Deploy → Apache server
