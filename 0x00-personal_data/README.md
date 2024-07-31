# ALX Backend User Data Project

## Overview

This project focuses on handling user data securely by implementing logging, data filtering, and password management practices. It covers techniques to protect Personally Identifiable Information (PII), manage logging with sensitive data, and securely handle passwords using hashing and validation.

## Project Structure

- `filtered_logger.py`: Contains functionality for logging, filtering PII, and connecting to a database.
- `encrypt_password.py`: Implements password hashing and validation using bcrypt.
- `main.py`: Main script to demonstrate the functionality of the project.

## Task Summary

1. **Regex-ing**
   - Write a function to obfuscate sensitive fields in log messages using regular expressions.

2. **Log Formatter**
   - Implement a custom log formatter to redact PII from log messages.

3. **Create Logger**
   - Set up a logger that uses the custom formatter and logs up to the INFO level.

4. **Connect to Secure Database**
   - Establish a connection to a MySQL database using credentials stored in environment variables.

5. **Read and Filter Data**
   - Retrieve and display data from the database with sensitive fields redacted.

6. **Encrypting Passwords**
   - Implement password hashing using bcrypt.

7. **Check Valid Password**
   - Implement password validation against hashed passwords using bcrypt.

## Setup and Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/alx-backend-user-data.git
   cd alx-backend-user-data
   ```

2. **Install Dependencies**

   Make sure you have `mysql-connector-python` and `bcrypt` installed.

   ```bash
   pip3 install mysql-connector-python bcrypt
   ```

3. **Setup MySQL Database**

   Use the provided `main.sql` file to set up your MySQL database. Execute the following commands:

   ```bash
   mysql -uroot -p < main.sql
   ```

4. **Set Environment Variables**

   Set the following environment variables for database credentials:

   ```bash
   export PERSONAL_DATA_DB_USERNAME=root
   export PERSONAL_DATA_DB_PASSWORD=root
   export PERSONAL_DATA_DB_HOST=localhost
   export PERSONAL_DATA_DB_NAME=my_db
   ```

## Usage

1. **Run `main.py` to Test Filtering**

   ```bash
   ./main.py
   ```

   This will demonstrate the filtering of PII in log messages.

2. **Run `filtered_logger.py` to Test Data Retrieval**

   ```bash
   ./filtered_logger.py
   ```

   This will connect to the database, retrieve user data, and display it with sensitive fields redacted.

## Files

- `filtered_logger.py`: Implements logging with redaction and database connection.
- `encrypt_password.py`: Handles password hashing and validation.
- `main.py`: Demonstrates functionality for both filtering and encryption tasks.

## Code Style

The code adheres to the PEP 8 style guide and uses `pycodestyle` for validation.

## Documentation

Each module, class, and function includes detailed documentation to explain their purpose and usage.