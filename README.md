# python_bank_code

## Table of Contents
1. [Introduction](#1-introduction)
2. [Project Overview](#2-project-overview)
3. [Code Analysis](#3-code-analysis)
4. [Strengths](#4-strengths)
5. [Areas for Improvement](#5-areas-for-improvement)
6. [Future Plans](#6-future-plans)
7. [Usage Instructions](#7-usage-instructions)
8. [Testing](#8-testing)
9. [Conclusion](#9-conclusion)

---

## 1. Introduction

### 1.1 Project Background
This project simulates core banking operations through a text-based interface. It is designed for personal or educational purposes, serving as a practical exercise in Python programming.

### 1.2 Project Objectives
The primary objectives of this project are:
- Allowing users to register and create new bank accounts with a username and password.
- Enabling registered users to log in securely.
- Providing logged-in users options to deposit money, withdraw money, and check account balances.
- Persisting user credentials and balance information between sessions using files.

### 1.3 Scope
The scope is limited to core banking functions via a command-line interface (CLI). It does not include advanced features such as transaction history, fund transfers, or interest calculations.

---

## 2. Project Overview

### 2.1 Core Functionality
- **Account Creation:** Users can create accounts with unique usernames and passwords. Credentials are stored in `username_password.txt`, and balances are initialized to 0 in `balance.txt`.
- **Login:** Validates username and password against stored data.
- **Deposit:** Adds funds to the user's account and updates `balance.txt`.
- **Withdrawal:** Deducts funds while ensuring sufficient balance, and updates `balance.txt`.
- **Balance Check:** Displays the current balance of the logged-in user.

### 2.2 Technology Stack
- Python 3
- Standard Python libraries for file handling and input/output.

### 2.3 Architecture
- Procedural programming paradigm.
- Function-based organization within a single script (`main.py`).

### 2.4 User Interface
- Command-line based interaction using text prompts.

---

## 3. Code Analysis

### 3.1 Structure and Organization
- Functions encapsulate different operations (e.g., `signup`, `login`, `deposit`).
- Global variables are used, which can complicate state management.
- Data is stored in plain text files (`username_password.txt`, `balance.txt`).

### 3.2 Readability and Maintainability
- Variable and function names are descriptive.
- Some comments exist, but there is room for improvement.
- Global variables and direct file manipulation reduce maintainability.

### 3.3 Data Handling
- **Persistence:** Achieved using plain text files.
- **Security:** Passwords are stored in plain text, which is insecure.
- **Integrity:** No mechanisms for handling file corruption or concurrent access.
- **Efficiency:** Updating entire files for small changes is inefficient.

### 3.4 Error Handling and Robustness
- Basic checks for existing usernames, incorrect passwords, and insufficient funds.
- Limited input validation; non-numeric inputs can cause runtime errors.
- No explicit handling of file I/O errors.

---

## 4. Strengths
- **Simplicity:** Easy to understand for beginners.
- **Functionality:** Achieves basic objectives of simulating simple banking tasks.
- **Demonstrates Core Concepts:** Covers functions, loops, conditionals, basic file I/O, and user input handling.
- **Self-Contained:** Runs without external dependencies.

---

## 5. Areas for Improvement

### 5.1 Security
- Implement password hashing (e.g., using `hashlib` or `bcrypt`).
- Encrypt sensitive data stored in files.

### 5.2 Data Management
- Use structured data formats like JSON or SQLite for better organization.
- Implement data integrity checks and backups.

### 5.3 Code Structure and Design
- Refactor using Object-Oriented Programming (OOP) for better scalability.
- Eliminate global variables and pass data explicitly.
- Modularize the code by splitting it into multiple files (e.g., `data_manager.py`, `auth.py`).

### 5.4 Error Handling and Robustness
- Validate all user inputs and handle exceptions gracefully.
- Use `try...except` blocks for file operations and input parsing.

### 5.5 Features
- Add transaction history with timestamps.
- Allow fund transfers between accounts.
- Improve user experience with clearer prompts and feedback messages.

---

## 6. Future Plans
- Introduce unit tests using `unittest` or `pytest`.
- Add support for advanced banking features like interest calculations.
- Implement a graphical user interface (GUI) for better usability.

---

## 7. Usage Instructions

### Prerequisites
- Python 3 installed on your system.

### Steps to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/hrishabh-dev/python_bank_code.git
   cd python_bank_code
