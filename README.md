User Management API
This project implements a RESTful API for user management using Node.js, Express, and MongoDB. The API provides endpoints to create, read, update, and delete user information, along with user authentication.

Table of Contents
Introduction
Features
Installation
Usage
API Endpoints
Project Structure
Introduction
The User Management API is designed to handle user-related operations, including user registration, login, profile management, and CRUD operations on user data. The API is built with Node.js and Express, with MongoDB as the database.

Features
User registration and authentication
Create, read, update, and delete user information
Secure password hashing
JWT-based authentication
Installation
Clone the repository:
git clone https://github.com/Chukwuskindall/user-management-restapi.git
cd User-Management-Api
Install dependencies:
npm install
Set up environment variables:
Create a .env file in the root directory and add your environment variables:

MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
PORT=5000
Run the application:
npm start
The server will start on http://localhost:5000.

Usage
Use tools like Postman or cURL to interact with the API. The base URL for the API is http://localhost:5000.

API Endpoints
Auth
POST /api/auth/register: Register a new user
POST /api/auth/login: Log in a user
Users
GET /api/users: Retrieve all users (authenticated users only)
GET /api/users/:id: Retrieve a specific user (authenticated users only)
PUT /api/users/:id: Update a user's information (authenticated users only)
DELETE /api/users/:id: Delete a user (authenticated users only)
Project Structure
User-Management-Api/
│
├── controllers/             # Controller files for handling requests
│   ├── authController.js    # Auth-related request handling
│   ├── userController.js    # User-related request handling
│
├── models/                  # Database models
│   ├── userModel.js         # User model schema
│
├── routes/                  # Route definitions
│   ├── authRoutes.js        # Auth-related routes
│   ├── userRoutes.js        # User-related routes
│
├── middlewares/             # Middleware functions
│   ├── authMiddleware.js    # Authentication middleware
│
├── config/                  # Configuration files
│   ├── db.js                # Database connection setup
│
├── .env                     # Environment variables
├── server.js                # Main server file
├── package.json             # Project dependencies
└── README.md                # Project README file
