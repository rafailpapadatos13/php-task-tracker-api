# 📋 Task & Issue Tracker API (CRUD Application)

A full-stack, lightweight Task and Issue Management web application built with a native PHP RESTful API backend, MySQL database via PDO, and a dynamic HTML5/JS single-page frontend.

---

## 🚀 Features

- **Full CRUD Functionality**: Create, read, update status, and delete tasks in real-time.
- **RESTful API Architecture**: Native PHP endpoint (`api.php`) supporting `GET`, `POST`, and `DELETE` requests.
- **Secure Database Layer**: MySQL interaction via **PDO** using prepared statements to prevent SQL Injection.
- **Asynchronous UI**: Dynamic interface powered by vanilla JavaScript (`Fetch API`) without page reloads.
- **Clean Responsive UI**: Modern dashboard layout for intuitive task organization.

---

## 🛠️ Tech Stack

- **Backend**: PHP 8.x (RESTful API, PDO)
- **Database**: MySQL / MariaDB
- **Frontend**: HTML5, CSS3, Vanilla JavaScript (ES6+, Fetch API)
- **Environment**: Laragon / Apache

---

## ⚙️ Database Schema

```sql
CREATE DATABASE IF NOT EXISTS task_db;
USE task_db;

CREATE TABLE IF NOT EXISTS tasks (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    description TEXT NULL,
    status ENUM('pending', 'in_progress', 'completed') DEFAULT 'pending',
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
