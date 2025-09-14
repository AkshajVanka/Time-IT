# Time-IT

Time-IT is a full-stack MERN application designed for effective time and task management. It provides a user-friendly interface to help users organize their tasks, schedule their time, and improve productivity.

## Features

*   **User Authentication:** Secure user registration and login using JSON Web Tokens (JWT).
*   **Task Management:** Create, update, and delete tasks with details such as task name, description, priority, and due date.
*   **Time Scheduling:** Allocate specific time slots for tasks.
*   **Dashboard:** An intuitive dashboard to view and manage daily tasks.
*   **Calendar View:** A visual calendar to see scheduled tasks.
*   **Reporting:** Generate reports to track task completion and time usage.

## Technologies Used

### Backend

*   **Node.js:** JavaScript runtime for the server.
*   **Express:** Web framework for Node.js.
*   **MongoDB:** NoSQL database for storing user and task data.
*   **Mongoose:** Object Data Modeling (ODM) library for MongoDB.
*   **bcryptjs:** Library for hashing passwords.
*   **jsonwebtoken:** For creating and verifying JSON Web Tokens.
*   **config:** For managing configuration variables.
*   **express-validator:** For validating incoming request data.

### Frontend

*   **React:** JavaScript library for building user interfaces.
*   **Redux:** For state management.
*   **React Router:** For client-side routing.
*   **Axios:** For making HTTP requests to the backend API.
*   **Moment.js:** For working with dates and times.
*   **React-Bootstrap:** For UI components.

## Prerequisites

*   Node.js and npm
*   MongoDB

## Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/Time-IT.git
    cd Time-IT
    ```

2.  **Install backend dependencies:**
    ```bash
    npm install
    ```

3.  **Install frontend dependencies:**
    ```bash
    cd client
    npm install
    cd ..
    ```

4.  **Set up configuration:**
    Create a `default.json` file in the `config` directory with your MongoDB connection string and JWT secret:
    ```json
    {
      "mongoURI": "your-mongodb-connection-string",
      "jwtSecret": "your-jwt-secret"
    }
    ```

## Usage

1.  **Run the development server:**
    ```bash
    npm run dev
    ```
    This will start both the backend and frontend servers concurrently.

2.  **Open your browser** and navigate to `http://localhost:3000`.

## API Endpoints

### Auth

*   `POST /api/auth`: Authenticate a user and get a token.
*   `GET /api/auth`: Get the authenticated user's data.

### Users

*   `POST /api/users`: Register a new user.
*   `PUT /api/users/addtask`: Add a new task for the user.
*   `DELETE /api/users/deletetask/:id`: Delete a task by its ID.
*   `PUT /api/users/updatetask`: Update a task.
*   `GET /api/users/gettasks/:startDate/:endDate`: Get all tasks within a specified date range.

## Folder Structure

```
/
├── client/         # React frontend
├── config/         # Database and other configurations
├── middleware/     # Express middleware
├── models/         # Mongoose models
├── routes/         # API routes
├── server.js       # Backend entry point
└── package.json
```

## Available Scripts

*   `npm start`: Starts the backend server.
*   `npm run server`: Starts the backend server with nodemon for development.
*   `npm run client`: Starts the frontend development server.
*   `npm run dev`: Starts both the backend and frontend servers concurrently.
*   `npm run heroku-postbuild`: Builds the React app for production.
```