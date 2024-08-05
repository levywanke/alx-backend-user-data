# Basic Authentication API

### Project Overview

This project focuses on implementing Basic Authentication for a simple API. The purpose is to understand the authentication process and implement it manually for learning purposes. In a real-world scenario, it’s advisable to use established modules or frameworks (e.g., Flask-HTTPAuth in Python-Flask) for such tasks.

### Learning Objectives

By the end of this project, you should be able to explain:
- What authentication means
- What Base64 is and how to encode a string in Base64
- What Basic authentication means
- How to send the Authorization header in an HTTP request

### Requirements

- **Python Scripts:**
  - Files will be interpreted/compiled on Ubuntu 18.04 LTS using Python 3.7
  - Files must end with a new line
  - The first line of all files should be `#!/usr/bin/env python3`
  - Follow the `pycodestyle` style (version 2.5)
  - All files must be executable
  - Use `wc` to test the length of files
  - All modules, classes, and functions must have proper documentation

### Setup and Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/alx-backend-user-data.git
   ```

2. **Navigate to the project directory:**
   ```bash
   cd alx-backend-user-data/0x01-Basic_authentication
   ```

3. **Install dependencies:**
   ```bash
   pip3 install -r requirements.txt
   ```

4. **Start the server:**
   ```bash
   API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
   ```

5. **Use the API:**
   ```bash
   curl "http://0.0.0.0:5000/api/v1/status"
   ```

### Tasks

1. **Simple-basic-API**
   - Implement a simple API with Basic Authentication.
   - Setup and test the API as described in the project requirements.

2. **Error Handler: Unauthorized**
   - Add an error handler for HTTP status code 401.
   - Implement a route to test this error handler.

3. **Error Handler: Forbidden**
   - Add an error handler for HTTP status code 403.
   - Implement a route to test this error handler.

4. **Auth Class**
   - Create an `Auth` class with methods to handle authentication-related tasks.

5. **Define Non-Authenticated Routes**
   - Update the `require_auth` method to manage paths that don't need authentication.

6. **Request Validation**
   - Validate requests by checking for the `Authorization` header and handle errors.

7. **Basic Auth Class**
   - Create a `BasicAuth` class inheriting from `Auth`.

8. **Base64 Encoding/Decoding**
   - Implement methods to handle Base64 encoding and decoding in the `BasicAuth` class.

### Repository Structure

- **`api/v1/`**: Contains the main API implementation and authentication logic.
- **`api/v1/auth/`**: Contains authentication classes and methods.
- **`api/v1/views/`**: Contains routes and endpoints.
- **`requirements.txt`**: Lists the project dependencies.
- **`README.md`**: This file.

### Testing

To test the different functionalities, use the provided `main_x.py` scripts as described in the task sections.

