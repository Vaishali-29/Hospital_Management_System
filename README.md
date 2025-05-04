# 🏥 Hospital Management System (Java + JDBC + MySQL)

A simple console-based Hospital Management System built using Java and JDBC, designed to handle basic operations like managing patients and appointments. This project demonstrates how Java can be used to interact with a MySQL database for CRUD operations.

---

## 📌 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Database Setup](#database-setup)
- [Usage](#usage)
- [Contributing](#contributing)

---

## ✅ Features

- ➕ Add New Patient
- 📋 View All Patients
- 🗓️ Book Appointments
- ❌ Delete Patient Records
- ✏️ Update Patient Information
- 📦 Simple Command Line Interface

---

## 🛠 Tech Stack

- **Language**: Java
- **Database**: MySQL
- **Connectivity**: JDBC (Java Database Connectivity)
- **IDE**: IntelliJ IDEA / Eclipse / NetBeans
- **Build Tool**: None (simple .java files) or optionally Maven

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/hospital-management-system-java.git
cd hospital-management-system-java
```

### 2. Open in your preferred Java IDE

- Make sure you have the MySQL JDBC driver (`mysql-connector-java`) added to your project libraries.

### 3. Configure database credentials

In your main Java file or DB utility class, update the following:
```java
String url = "jdbc:mysql://localhost:3306/hospital";
String user = "your_db_username";
String password = "your_db_password";
```

---

## 🛠️ Database Setup

1. Open MySQL Workbench or your preferred SQL tool.
2. Create a new database:
```sql
CREATE DATABASE hospital;
```
3. Use the SQL script in `database/hospital.sql` to create the required tables:
```sql
USE hospital;

CREATE TABLE patients (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10),
    contact VARCHAR(20)
);

CREATE TABLE appointments (
    id INT PRIMARY KEY AUTO_INCREMENT,
    patient_id INT,
    appointment_date DATE,
    doctor_name VARCHAR(100),
    FOREIGN KEY (patient_id) REFERENCES patients(id)
);
```

---

## 💻 Usage

Compile and run your main file:

```bash
javac Main.java
java Main
```

> The program will launch a menu-driven console interface where you can choose options like adding a patient, viewing records, booking an appointment, etc.


---

## 🤝 Contributing

Contributions are welcome!

1. Fork this repo
2. Create your feature branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature-name`)
5. Open a Pull Request

---


## 📬 Contact

Created by Vaishali Awasthi – contact at [awastivaishali@gmail.com].

