# 🏦 Bank Management System

A simple **Command-Line Interface (CLI)** based **Bank Management System** in Python with MySQL backend. This project simulates core banking operations like user registration, login, money withdrawal/deposit, transaction tracking, profile management, and account deletion.

---

## 📌 Features

✅ User Registration (Sign-Up)  
✅ User Authentication (Login)  
✅ Deposit and Withdraw Money  
✅ View Last 5 Transactions  
✅ View and Update Profile Details  
✅ Delete Account  
✅ Secure Password Validation  
✅ Error Handling and Input Validation

---

## ⚙️ Tech Stack

- **Language**: Python 3
- **Database**: MySQL
- **Libraries Used**:
  - `mysql.connector` – Database connectivity
  - `datetime` – Date and time handling
  - `curses.ascii`, `distutils.log`, `ast` – Input validation and error handling

---

## 🗃️ Database Setup

### 🔸 Create Database

```sql
CREATE DATABASE hubnet;
USE hubnet;
```

### 🔸 Table: `bank`

```sql
CREATE TABLE bank (
    Name VARCHAR(50),
    UserName VARCHAR(50) PRIMARY KEY,
    Password VARCHAR(50),
    DOB DATE,
    Address TEXT,
    Mobile_Number VARCHAR(10),
    Aadhar_no VARCHAR(12),
    Balance INT
);
```

### 🔸 Table: `transaction`

```sql
CREATE TABLE transaction (
    Credited INT,
    Debited INT,
    UserName1 VARCHAR(50),
    Date DATETIME,
    FOREIGN KEY (UserName1) REFERENCES bank(UserName)
);
```

---

## 🔐 Password Rules

Passwords must include:
- ✅ At least 1 **uppercase** letter  
- ✅ At least 1 **lowercase** letter  
- ✅ At least 1 **digit**  
- ✅ At least 1 **special symbol** (`@`, `$`, `#`, `%`)  
- ✅ Minimum **6 characters**

---

## 🖥️ How to Run

1. **Ensure MySQL is installed** and running.
2. **Create the database and tables** using the schema above.
3. Update database credentials in the script:

```python
mycon = sql.connect(
    host="localhost",
    user="root",
    password="12345678",
    database="hubnet"
)
```

4. Run the script:

```bash
python.py
```

---

## 🧪 Example Usage

```
Welcome To Bank Management System

Press 1 to Sign Up
Press 2 to Sign In
```

- After logging in, you'll be prompted with options like:
  - Withdraw money
  - Deposit money
  - View profile
  - Update details
  - View last 5 transactions
  - Delete account
  - Logout

---

## 🛠️ Improvements To Consider

- ✅ Refactor into functions or classes (Object-Oriented Design)
- ✅ Hash passwords instead of storing plaintext
- ✅ Improve transaction history filtering (e.g., show only last 5)
- ✅ Add GUI using Tkinter / PyQt or web interface using Flask / Django
- ✅ Use environment variables for DB credentials

---

## 📂 Project Structure (suggested)

```
Bank-Management-System/
├── bank.py                  # Main application script
├── README.md                # Project README
└── requirements.txt         # (Optional) Python dependencies
```

---

## 🧑‍💻 Author

**Gattu Hruthik Rohith**  
[GitHub Repository → Bank Management System](https://github.com/Hruthikrohith/Bank-Management-System)

---

## 📃 License

This project is for educational purposes. You can use and modify it freely. If you use this project, consider giving credit.

---

## ⭐ Star This Repo

If you found this helpful, please consider giving the repository a ⭐ on GitHub!

---
