# User Status Toggle Web App (PHP + MySQL)

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
- Toggle button for each record to update the `status` value between 0 and 1
- Changes reflect immediately on the page after toggling

---

## ⚙️ How to Run (Using XAMPP)

1. **Download or Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/user-status-toggle-xampp.git
   
2. **Move the folder to your XAMPP htdocs directory**
   
Place the project folder into your XAMPP htdocs directory:
   
C:\xampp\htdocs\user-status-toggle-xampp

3. **Start Services**
Open the XAMPP Control Panel and start:
-Apache
-MySQL

4. **Set Up the Database**
   
1-Go to http://localhost/phpmyadmin

2-Create a new database called: employee_db

3-Run this SQL code to create the table:

CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    age INT,
    status TINYINT(1) DEFAULT 0
);

5. **Configure Database Connection**
Edit your PHP code (index.php or db.php) to connect to the database:

<?php
$conn = new mysqli("localhost", "root", "", "employee_db");
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
?>

6. **Open in Your Browser**
http://localhost/user-status-toggle-xampp/index.php

📁 Project Structure

user-status-toggle-xampp/
├── index.php           # Main form and data table
└── toggle.php          # Script to toggle status

