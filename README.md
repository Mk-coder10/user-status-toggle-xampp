# 🧩 User Status Toggle Web App (PHP + MySQL)

This is a simple PHP web application that allows users to:
- Submit their name and age through a form
- Display all employees from a MySQL database
- Toggle the status (0 or 1) for each user in real-time

> ✅ Built and tested using **XAMPP** on localhost.

---

## 📸 Screenshot

<img width="573" height="266" alt="image" src="https://github.com/user-attachments/assets/eefe7367-fe15-4e8c-b02a-9195042f8ff4" />

---

## 🛠 Technologies Used

- HTML / CSS  
- PHP  
- MySQL  
- XAMPP (Apache + MySQL)

---

## 🚀 Features

- One-line input form (Name, Age)  
- Stores records into a MySQL database  
- Displays all records in a table  
- Toggle button for each record to update the `status` between 0 and 1  
- Changes reflect immediately after toggling  

---

## ⚙️ How to Run (Using XAMPP)

### 1. Download the ZIP File

Click the green **Code** button in the GitHub repo, then choose **Download ZIP**.  
Extract it anywhere on your computer.

---

### 2. Start XAMPP Services

Open **XAMPP Control Panel** and start:
- Apache  
- MySQL  

---

### 3. Set Up the Database

1. Go to: http://localhost/phpmyadmin  
2. Create a new database called: `employee_db`  
3. Run this SQL query:
CREATE TABLE employees (
id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(100),
age INT,
status TINYINT(1) DEFAULT 0
);


---

### 4. Configure Database Connection

In your `index.php` file (or `db.php`), use this connection code:

<?php $conn = new mysqli("localhost", "root", "", "employee_db"); if ($conn->connect_error) { die("Connection failed: " . $conn->connect_error); } ?>


---

### 5. Open the Project in Your Browser

Put the extracted folder into this path:

Then open your browser and go to:

http://localhost/employee_app/index.php


## 📁 Project Structure

user-status-toggle-xampp/
├── index.php # Main form and table display
└── toggle.php # Script to toggle status

