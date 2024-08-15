# User Authentication Service

This project involves building a user authentication service using Flask and SQLAlchemy. The purpose is to understand authentication mechanisms by implementing a basic system for learning purposes.

## Project Overview

### Specializations

- **Focus:** User Authentication Service

### Project Details

## Learning Objectives

By the end of this project, you should be able to:
- Declare API routes in a Flask app.
- Get and set cookies.
- Retrieve request form data.
- Return various HTTP status codes.

## Requirements

- **Editors:** vi, vim, emacs
- **Interpreter:** Ubuntu 18.04 LTS, Python 3.7
- **File Endings:** All files must end with a new line.
- **Shebang:** All files should start with `#!/usr/bin/env python3`.
- **Style:** Code should follow `pycodestyle` version 2.5.
- **Database:** Use SQLAlchemy 1.3.x.
- **Executability:** All files must be executable.
- **Documentation:** Modules, classes, and functions must be documented.
- **Type Annotations:** All functions should be type annotated.
- **Flask Interaction:** Flask app should only interact with the Auth and DB classes, never directly with the database.

## Setup

1. Install the necessary Python packages:
    ```bash
    pip3 install bcrypt
    ```

## Project Tasks

### 0. User Model

Create a SQLAlchemy model named `User` with the following attributes:
- `id`: integer primary key
- `email`: non-nullable string
- `hashed_password`: non-nullable string
- `session_id`: nullable string
- `reset_token`: nullable string

### 1. Create User

Implement the `add_user` method in the `DB` class to add users to the database.

### 2. Find User

Implement the `find_user_by` method in the `DB` class to retrieve users based on arbitrary keyword arguments.

### 3. Update User

Implement the `update_user` method in the `DB` class to update user attributes.

### 4. Hash Password

Define a `_hash_password` method to hash passwords using bcrypt.

### 5. Register User

Implement the `register_user` method in the `Auth` class to register new users.

### 6. Basic Flask App

Set up a basic Flask app with a single GET route ("/") that returns a JSON payload: `{"message": "Bienvenue"}`.

### 7. Register User Endpoint

Implement a POST `/users` endpoint to register new users using the `Auth` class.

### 8. Credentials Validation

Implement the `valid_login` method in the `Auth` class to validate user credentials.

### 9. Generate UUIDs

Implement a `_generate_uuid` method in the `Auth` class to generate new UUIDs.

### 10. Get Session ID

Implement the `create_session` method in the `Auth` class to generate a session ID for users.

### 11. Log In

Implement a POST `/sessions` endpoint to log in users and set a session cookie.

## Repo Structure

- **GitHub Repository:** [alx-backend-user-data](https://github.com/your-repo/alx-backend-user-data)
- **Directory:** `0x03-user_authentication_service`
- **Files:**
  - `user.py` - SQLAlchemy `User` model
  - `db.py` - Database interactions
  - `auth.py` - Authentication logic
  - `app.py` - Flask application

## Usage

1. Run the Flask application:
    ```bash
    python3 app.py
    ```
2. Use `curl` or a similar tool to interact with the endpoints.