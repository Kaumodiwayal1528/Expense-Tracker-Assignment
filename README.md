# Expense-Tracker-Assignment
# Expense Tracker Application

## Description

This is a full-stack expense tracker application that allows users to record their expenses and visualize their spending patterns.

## Features

* Add, edit, and delete expense records.
* Visualize expense data with charts (pie chart for category distribution, bar chart for monthly expenses).
* Responsive and user-friendly interface.

## Technologies Used

* **Frontend**: React
* **Backend**: Node.js, Express.js
* **Database**: MongoDB or PostgreSQL
* **UI Library**: Shadcn/UI
* **Chart Library**: Recharts
* **Styling**: Tailwind CSS

## Prerequisites

* Node.js and npm installed
* MongoDB or PostgreSQL installed and running
* Basic knowledge of React, Node.js, Express.js, and database concepts

## Setup Instructions

1.  **Clone the repository (if applicable)**

    * If you have the code in a Git repository, clone it to your local machine:
        ```bash
        git clone <repository_url>
        cd expense-tracker
        ```

2.  **Set up the backend**

    * Navigate to the backend folder:
        ```bash
        cd backend  # If you have a separate backend folder
        ```
    * Install backend dependencies:
        ```bash
        npm install
        ```
    * Configure the database:
        * Create a `config.js` or `.env` file with your database connection details.  For example (for MongoDB):
            ```javascript
            // config.js
            module.exports = {
              database: {
                url: 'mongodb://username:password@localhost:27017/your-database-name', // Or your connection string
              },
              port: 3001, // Or your preferred port
            };
            ```
        * Or for a `.env` file:
             ```
             # .env
             DB_URL=postgres://user:password@host:port/database
             PORT=3001
             ```
    * Start the backend server:
        ```bash
        npm start
        ```
        * The backend server should be running at `http://localhost:3001` (or the port you configured).

3.  **Set up the frontend**

    * Navigate to the frontend folder:
        ```bash
        cd frontend  # If you have a separate frontend folder
        ```
    * Install frontend dependencies:

        ```bash
        npm install
        ```
    * Configure the API base URL:
        * In `frontend/src/App.js` (or wherever your main component is), make sure the `API_BASE_URL` constant matches the URL of your backend server:
        ```javascript
        const API_BASE_URL = 'http://localhost:3001'; // Make sure this is correct
        ```
    * Start the frontend development server:
        ```bash
        npm start
        ```
    * The frontend application should be running at `http://localhost:3000` (or another port, depending on your setup).

4.  **Access the application**

    * Open your browser and go to the URL where the frontend application is running (e.g., `http://localhost:3000`).

##  Important Notes

* **Backend Setup is Crucial**: This README assumes you have a working backend.  The React code provided needs a backend to function.  Make sure your Node.js/Express.js server and database are set up correctly.
* **Database**:  This application supports either MongoDB or PostgreSQL.  You'll need to choose one and configure the backend accordingly.  The provided React code doesn't include database setup; that's part of the backend implementation.
* **API Base URL**:  Double-check that the `API_BASE_URL` in the React code matches the actual URL where your backend server is running.  If they don't match, the frontend won't be able to communicate with the backend.
* **CORS**: If you encounter Cross-Origin Resource Sharing (CORS) errors, you'll need to configure your Express.js backend to allow requests from the frontend's origin.
* **Error Handling**:  The code includes basic error handling (e.g., alerts for failed requests).  For a production application, you'd want more robust error handling.
* **Dependencies**:  Make sure you have all the required dependencies installed for both the frontend and backend.  The `npm install` commands in the instructions will help you with this.
