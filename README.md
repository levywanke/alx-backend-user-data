# ALX Backend User Data

## Overview

The ALX Backend User Data project focuses on securely managing user data through effective logging and password handling. The project implements practices for filtering Personally Identifiable Information (PII), logging with sensitive data protection, and securing passwords using encryption techniques.

## Key Components

1. **Logging and Data Filtering**
   - **`filtered_logger.py`**: Contains functions and classes for filtering PII from logs and connecting to a MySQL database.
   - **`main.py`**: Demonstrates how to use the logging and filtering functionality.

2. **Password Management**
   - **`encrypt_password.py`**: Implements password hashing and validation using bcrypt.
   - **`main.py`**: Includes examples of hashing and validating passwords.

## Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/alx-backend-user-data.git
   cd alx-backend-user-data
   ```

2. **Install Dependencies**

   ```bash
   pip3 install mysql-connector-python bcrypt
   ```

3. **Setup Database**

   Import the provided `main.sql` to set up the database:

   ```bash
   mysql -uroot -p < main.sql
   ```

4. **Set Environment Variables**

   Configure the environment variables for database connection:

   ```bash
   export PERSONAL_DATA_DB_USERNAME=root
   export PERSONAL_DATA_DB_PASSWORD=root
   export PERSONAL_DATA_DB_HOST=localhost
   export PERSONAL_DATA_DB_NAME=my_db
   ```

## Usage

- **Filter and Format Logs**: Run `main.py` to see the log filtering and formatting in action.
- **Password Encryption**: Use `encrypt_password.py` to hash and validate passwords.