🏧 ATM Simulation Project
This Java console-based project simulates the core functionalities of an ATM (Automated Teller Machine), including authentication, balance inquiry, deposit, withdrawal, and receipt printing — all integrated with a MySQL database using JDBC.

📌 Features
🔐 PIN-based user authentication

💰 Balance inquiry

➕ Deposit amount

➖ Withdraw amount (with insufficient balance check)

🧾 Receipt generation (transaction summary)

💾 Real-time updates to the database using JDBC

🛠️ Technologies Used
Language: Java

Database: MySQL

Connectivity: JDBC (Java Database Connectivity)

IDE: IntelliJ IDEA / Eclipse (Recommended)

🗃️ Database Setup
Database Name: atm
Table Name: list
Required Columns in list table:

sql
Copy
Edit
ac_no INT PRIMARY KEY,    -- Account Number / PIN
...                        -- (Other fields like ID, etc.)
name VARCHAR(50),
balance INT
You can create the table like this:

sql
Copy
Edit
CREATE DATABASE atm;
USE atm;

CREATE TABLE list (
  ac_no INT PRIMARY KEY,
  name VARCHAR(50),
  balance INT
);

INSERT INTO list VALUES (1234, 'John Doe', 5000);
🧾 Project Structure
bash
Copy
Edit
atmProject/
├── atm.java              # Main application logic
└── module-info.java      # Java module declaration
▶️ How to Run
Ensure MySQL is running and a database named atm exists with the correct table (list).

Update the database credentials in the Java code:

java
Copy
Edit
Connection con = DriverManager.getConnection("jdbc:mysql://localhost:3306/atm", "root", "your_password_here");
Compile and run the program:

bash
Copy
Edit
javac atm.java
java atm
💡 Sample Use Flow
Enter your PIN (e.g., 1234).

Choose an option:

1 → Check balance

2 → Add amount

3 → Withdraw amount

4 → Print receipt

5 → Exit

📌 Notes
JDBC MySQL connector is required. Add it to your classpath or import as a library.

Error handling and input validation are basic — for educational purposes.

Replace hardcoded DB credentials with secure config for real applications.

📃 License
This project is intended for learning and educational purposes only.
