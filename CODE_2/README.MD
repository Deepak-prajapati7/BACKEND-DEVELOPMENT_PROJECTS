Student Management REST API

Lab Assignment 2 – Student Management REST API

Subject: Web Dev III (Node.js & Express Backend)
Unit: 2
Technology: Node.js, Express.js, Postman

---

📌 Project Description

The Student Management REST API is a backend application developed using Node.js and Express.js.

This project provides REST API endpoints to perform CRUD operations on student records:

- Create a student
- View all students
- View a student by ID
- Update a student
- Delete a student

The project uses an array/JSON data structure instead of a database, as required by the assignment.

---

🎯 Learning Objectives

- Understand Express.js server setup
- Build REST APIs
- Perform CRUD operations
- Use middleware
- Implement modular routing
- Handle errors and HTTP status codes
- Test APIs using Postman

---

🛠️ Technologies Used

- Node.js
- Express.js
- JavaScript
- Postman
- JSON
- In-memory Array

---

📂 Project Structure

ASSIGNMENT_2/
│
├── app.js
├── package.json
│
├── routes/
│   └── studentRoutes.js
│
├── middleware/
│   └── logger.js
│
└── data/
    └── students.js

---

🚀 Installation

1. Clone the repository

git clone <YOUR_GITHUB_REPOSITORY_URL>

2. Navigate to the project directory

cd ASSIGNMENT_2

3. Install dependencies

npm install

4. Start the server

node app.js

The server will run on:

http://localhost:3000

---

🔗 API Endpoints

Method| Endpoint| Description
GET| "/students"| Get all students
GET| "/students/:id"| Get student by ID
POST| "/students"| Add a new student
PUT| "/students/:id"| Update a student
DELETE| "/students/:id"| Delete a student

These are the CRUD APIs required by the assignment.

---

📥 GET All Students

Request

GET http://localhost:3000/students

Example Response

[
  {
    "id": 1,
    "name": "Rahul",
    "email": "rahul@example.com",
    "course": "BCA"
  },
  {
    "id": 2,
    "name": "Priya",
    "email": "priya@example.com",
    "course": "BCA"
  }
]

---

🔍 GET Student by ID

Request

GET http://localhost:3000/students/1

Example Response

{
  "id": 1,
  "name": "Rahul",
  "email": "rahul@example.com",
  "course": "BCA"
}

If the student does not exist, the API returns:

404 Not Found

---

➕ POST Create Student

Request

POST http://localhost:3000/students

Headers

Content-Type: application/json

Request Body

{
  "name": "Amit",
  "email": "amit@example.com",
  "course": "BCA"
}

Response

201 Created

Example:

{
  "id": 3,
  "name": "Amit",
  "email": "amit@example.com",
  "course": "BCA"
}

---

✏️ PUT Update Student

Request

PUT http://localhost:3000/students/1

Headers

Content-Type: application/json

Request Body

{
  "name": "Rahul Sharma",
  "email": "rahulsharma@example.com",
  "course": "MCA"
}

Response

200 OK

---

🗑️ DELETE Student

Request

DELETE http://localhost:3000/students/1

Response

200 OK

Example:

{
  "message": "Student deleted successfully"
}

---

⚠️ HTTP Status Codes

The API uses appropriate HTTP status codes:

Status Code| Meaning
"200"| Successful request
"201"| Student successfully created
"400"| Bad request
"404"| Student or route not found

The assignment specifically requires these status codes for proper error handling.

---

🧩 Middleware

A custom logger middleware is used to log incoming HTTP requests.

Example output:

GET /students
POST /students
PUT /students/1
DELETE /students/1

The assignment requires implementation of a custom logger middleware.

---

🛣️ Modular Routing

Student routes are separated into:

routes/studentRoutes.js

The main application imports and uses these routes through Express Router.

This keeps the project organized and follows the modular routing requirement.

---

💾 Data Storage

No database is used in this project.

Student information is stored using an in-memory JavaScript array/JSON data structure.

This follows the assignment restriction:

- No MongoDB
- No MySQL
- No Mongoose
- Array and JSON data only

Note: Because the data is stored in memory, all changes are lost when the se
