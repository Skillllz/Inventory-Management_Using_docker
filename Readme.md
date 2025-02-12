# 📦 Inventory Management System (Dockerized)

## 🚀 Overview
This **Inventory Management System** is a Django-based web application containerized using **Docker**. It allows businesses to track and manage inventory efficiently. The project includes a **PostgreSQL database**, a **Gunicorn application server**, and **Docker Compose** for orchestration.

## 🛠️ Features
✅ **Django Backend** - Robust API and admin interface  
✅ **Dockerized Setup** - Easy deployment with Docker & Docker Compose  
✅ **PostgreSQL Database** - Scalable data management  
✅ **Gunicorn Server** - Efficient WSGI server for production  
✅ **Volume Management** - Persistent storage for media and database  

## 🏗️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/inventory-management-system.git
cd inventory-management-system
```

### 2️⃣ Create an `.env` File
```env
DB_NAME=inventory_db
DB_USER=admin
DB_PASSWORD=adminpassword
```

### 3️⃣ Build and Run Containers
```bash
docker-compose up --build -d
```

### 4️⃣ Apply Migrations & Create Superuser
```bash
docker-compose exec invenio-web python manage.py migrate
docker-compose exec invenio-web python manage.py createsuperuser
```

### 5️⃣ Access the Application
- **Web App**: `http://localhost:8000/`
- **Admin Panel**: `http://localhost:8000/admin/`

## 🛠️ Docker Services Explained

### `invenio-web` (Django + Gunicorn)
- Runs the Django backend application using Gunicorn.
- Mounts volumes for persistent media storage.

### `invenio-db` (PostgreSQL Database)
- Stores inventory data with **persistent volume**.
- Uses environment variables for configuration.

## 📜 License
This project is open-source and available under the **MIT License**.

## 📞 Support
For issues, open a GitHub **issue** or contact `pakhareshubham04@gmail.com`. 🚀

