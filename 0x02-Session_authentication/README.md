# Session Authentication Project


### Short Specializations



### Project Overview

This project focuses on implementing Session Authentication without using external modules. The purpose is to understand the underlying mechanisms of session authentication and cookies by building it from scratch.

### Background Context

In real-world scenarios, it's recommended to use established modules or frameworks for session authentication (e.g., Flask-HTTPAuth in Python-Flask). This project is a learning exercise to walk through the process of creating a session authentication system.

### Learning Objectives

By the end of this project, you should be able to explain:

- What authentication means
- What session authentication entails
- What cookies are
- How to send and parse cookies

### Requirements

- **Python Version:** 3.7 (Ubuntu 18.04 LTS)
- **File Requirements:**
  - All files must end with a new line.
  - The first line of all files should be `#!/usr/bin/env python3`.
  - Files must be executable.
  - Use `pycodestyle` for coding style.
- **Documentation:**
  - Modules, classes, and functions should have appropriate documentation.
  - Documentation should be complete sentences explaining the purpose of the code.

### Tasks

#### 0. Basic Authentication Endpoints

- **Objective:** Integrate Basic Authentication with existing endpoints.
- **Steps:**
  1. Copy work from project 0x06 (Basic Authentication).
  2. Add a new endpoint: `GET /users/me` to retrieve the authenticated User object.
  3. Update `api/v1/app.py` and `api/v1/views/users.py` as described.

#### 1. Empty Session Class

- **Objective:** Create a `SessionAuth` class as a placeholder.
- **Steps:**
  1. Implement an empty `SessionAuth` class inheriting from `Auth`.
  2. Update `api/v1/app.py` to use `SessionAuth` based on `AUTH_TYPE` environment variable.

#### 2. Create a Session

- **Objective:** Implement session creation and management.
- **Steps:**
  1. Add `create_session` method to `SessionAuth` class to generate session IDs.
  2. Ensure that the `user_id_by_session_id` dictionary is used for storage.

#### 3. User ID for Session ID

- **Objective:** Retrieve user IDs from session IDs.
- **Steps:**
  1. Implement `user_id_for_session_id` method in `SessionAuth` class.
  2. Use dictionary `.get()` method to retrieve user IDs.

#### 4. Session Cookie

- **Objective:** Manage session cookies.
- **Steps:**
  1. Add `session_cookie` method to `Auth` class to return cookie values.
  2. Define cookie name using `SESSION_NAME` environment variable.

### Testing

To test your implementation:

1. **Basic Authentication:**
   - Run `main_0.py` to verify user creation and basic auth.
   - Use `curl` commands to test API endpoints with and without authentication.

2. **Session Management:**
   - Run `main_1.py` and `main_2.py` to test session creation and user ID retrieval.
   - Use `curl` commands to validate session functionality.

3. **Cookie Handling:**
   - Run `main_3.py` to test session cookies.
   - Use `curl` commands to check cookie values.

### Repository

- **GitHub Repository:** [alx-backend-user-data](https://github.com/your-repository)
- **Directory:** `0x02-Session_authentication`
- **Files:**
  - `api/v1/app.py`
  - `api/v1/views/users.py`
  - `api/v1/auth/session_auth.py`
  - `api/v1/auth/auth.py`