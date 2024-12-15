# To-Do List Application with Authentication  

This project is a full-stack To-Do list application featuring user authentication and persistent storage for tasks.

## Features  

- **Authentication**: User login and account creation with secure password hashing using SHA256.  
- **Cookie-Based Session Management**: Persistent login sessions enabled through signed cookies.  
- **RESTful API**: Backend endpoints for managing tasks, authentication, and user data.  
- **Interactive Frontend**: A clean and intuitive interface for managing tasks.  

## Installation  

### Backend  

1. Navigate to the `backend` directory.  
2. Install the required dependencies:  
   ```bash
   npm install --save express-basic-auth cookie-parser
   ```  

### Frontend  

1. Navigate to the `to-do-list` directory.  
2. Install frontend dependencies:  
   ```bash
   npm install  
   npm audit fix --force  
   ```  

## Usage  

### Backend Setup  

1. Create a `users.json` file in the `backend` directory for user data persistence. A sample file might look like this:  
   ```json
   {
     "users": {
       "exampleUser": {
         "passwordHash": "5e884898da28047151d0e56f8dc6292773603d0d6aabbdd62a11ef721d1542d8"
       }
     }
   }
   ```  

2. Start the backend server:  
   ```bash
   npm start  
   ```  

### Frontend Setup  

1. Start the frontend development server:  
   ```bash
   npm start  
   ```  

2. Open the application in your browser at `http://localhost:3000`.  

### Testing Authentication  

1. Login with a username and password matching the credentials stored in `users.json`.  
2. Create new accounts or log in to manage tasks.  

## API Endpoints  

- **POST `/items`**: Add a new task (requires authentication).  
- **GET `/items`**: Retrieve tasks for the logged-in user.  
- **GET `/logout`**: End the user session.  

For detailed API usage, refer to the `services/api.js` file in the frontend.  

## Technologies Used  

- **Frontend**: React, Axios, JavaScript  
- **Backend**: Node.js, Express.js  
- **Authentication**: `express-basic-auth`, `cookie-parser`  
- **Persistence**: JSON-based data storage  

## Future Improvements  

- Integrate a database for scalable user and task storage.  
- Enhance frontend with additional task management features, such as priorities and deadlines.  
- Implement OAuth-based authentication for enhanced security.  
