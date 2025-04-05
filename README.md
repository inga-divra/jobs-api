# Jobs API

[Live Demo](https://jobs-api-9m1s.onrender.com)

A simple RESTful API for managing job listings, built with **Node.js**, **Express**, and **MongoDB**.

## Features

- **User authentication (JWT)**: Secure login and user registration.
- **CRUD operations**: Create, Read, Update, Delete job listings.
- **Custom error handling**: Centralized error handling to ensure smooth operation.
- **Protected routes**: Certain routes require user authentication via JWT tokens.
- **MongoDB connection**: Seamless integration with MongoDB using Mongoose ORM.

## Tech Stack

- **Node.js**: JavaScript runtime used for building the API.
- **Express.js**: Web framework for building RESTful APIs.
- **MongoDB & Mongoose**: NoSQL database and Mongoose for easy interaction.
- **JSON Web Tokens (JWT)**: Secure user authentication via tokens.
- **dotenv**: For managing environment variables.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/inga-divra/jobs-api.git
   cd jobs-api
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add your MongoDB connection string and JWT secret key:

   ```
   MONGO_URI=your-mongodb-connection-string
   JWT_SECRET=your-jwt-secret
   ```

4. Start the application:

   ```bash
   npm start
   ```

   The server should now be running at `http://localhost:3000`.

## API Endpoints

### Authentication

- `POST /api/v1/auth/register`: Register a new user.
- `POST /api/v1/auth/login`: Login an existing user and receive a JWT token.

### Job Listings

- `GET /api/v1/jobs`: Get all job listings (protected).
- `GET /api/v1/jobs/:id`: Get a single job listing by ID (protected).
- `POST /api/v1/jobs`: Create a new job listing (protected).
- `PUT /api/v1/jobs/:id`: Update an existing job listing (protected).
- `DELETE /api/v1/jobs/:id`: Delete a job listing (protected).

## Deployment

This API is deployed on Render.com. You can access the live version here: [Jobs API](https://jobs-api-9m1s.onrender.com).
