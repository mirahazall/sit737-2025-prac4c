Calculator Microservice

This microservice provides REST API endpoints for performing basic and advanced arithmetic operations, including:

Addition (+)
Subtraction (-)
Multiplication (*)
Division (/)
Exponentiation (**)
Modulo (%)
Square Root (sqrt)

The service is built using Node.js and Express.js and includes proper error handling and logging using winston.

Features
 - Supports multiple arithmetic operations 
 - Handles invalid inputs with meaningful error messages 
 - Implements logging for tracking requests and errors 
 - RESTful API architecture

Setup Instructions
-  Prerequisites
Ensure you have the following installed:
* Node.js (v14+ recommended)
* npm (Node Package Manager)

3. Installation
- Clone the repository and install dependencies:
git clone https://github.com/mirahazall/sit737-2025-prac4c

- cd sit737-2025-prac4c

- npm install

5. Run the Microservice
- Start the server:
node server.js

- The server will run on http://localhost:3000 by default.

API Endpoints
Perform Arithmetic Operations
- POST /add, /subtract, /multiply, /divide, /exponentiate, /modulo, /square-root

- Request Body:
{
  "number1": 10,
  "number2": 5
}

- Response:
{
  "result": 15
}

Errors:
If either number is missing or invalid, a 400 Bad Request error is returned.

Logging
The service logs all operations and errors using winston. Example log entry:
info: New addition operation requested: 10 + 5 = 15
error: Error in division operation: Division by zero is not allowed.

Error Handling
All endpoints return JSON-formatted error messages when an invalid request is made. Example:
{
  "error": "Invalid input. Please provide valid numbers."
}
