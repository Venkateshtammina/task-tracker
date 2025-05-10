# Task Tracker - MERN Stack Application

A full-stack task management application built with the MERN stack (MongoDB, Express.js, React.js, Node.js).

## Features

- User Authentication (Register/Login)
- Project Management
- Task Management
- Real-time Updates
- Responsive Design

## Prerequisites

Before running this project, make sure you have the following installed:
- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas account)
- npm or yarn package manager

## Environment Variables

In `.env` file in your backend directory and add the following variables:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
EMAIL_USER=your_email
EMAIL_PASS=your_email_password
NODE_ENV=development
```

### Steps to Get Environment Variables:

1. **PORT**
   - Default is 5000
   - You can change it if 5000 is already in use

2. **MONGO_URI**
   - Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
   - Create a free account or sign in
   - Create a new cluster (free tier)
   - Click "Connect" on your cluster
   - Choose "Connect your application"
   - Copy the connection string
   - Replace `<password>` with your database user's password
   - Replace `<dbname>` with your database name (e.g., "task-tracker")

3. **JWT_SECRET**
   - This is a secret key for JWT token generation
   - Create a strong random string
   - You can generate one using:
     ```bash
     node -e "console.log(require('crypto').randomBytes(32).toString('hex'))"
     ```
   - Or use any secure random string generator

4. **EMAIL_USER and EMAIL_PASS**
   - For Gmail:
     1. Go to your Google Account settings
     2. Enable 2-Step Verification if not already enabled
     3. Go to Security → App passwords
     4. Create a new app password for "Mail"
     5. Use your Gmail address as EMAIL_USER
     6. Use the generated app password as EMAIL_PASS
   - For other email providers:
     - Use your email address as EMAIL_USER
     - Use your email password or app-specific password as EMAIL_PASS

5. **NODE_ENV**
   - Use "development" for local development
   - Use "production" when deploying



## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd task-tracker
```

2. Install backend dependencies:
```bash
cd backend
npm install
```

3. Install frontend dependencies:
```bash
cd ../frontend
npm install
```

## Running the Application

### Development Mode

1. Start the backend server:
```bash
cd backend
npm run dev or if that did not work node server.js
```

2. In a new terminal, start the frontend:
```bash
cd frontend
npm start
```

The application will be available at:
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000



## API Endpoints

### Authentication
- POST /api/auth/register - Register a new user
- POST /api/auth/login - Login user

### Projects
- GET /api/projects - Get all projects
- POST /api/projects - Create new project
- PUT /api/projects/:id - Update project
- DELETE /api/projects/:id - Delete project

### Tasks
- GET /api/tasks - Get all tasks
- POST /api/tasks - Create new task
- PUT /api/tasks/:id - Update task
- DELETE /api/tasks/:id - Delete task

## Technologies Used

- **Frontend:**
  - React.js
  - Redux Toolkit
  - Material-UI
  - Axios

- **Backend:**
  - Node.js
  - Express.js
  - MongoDB
  - Mongoose
  - JWT Authentication

## Project Structure

```
task-tracker/
├── frontend/          # React frontend
├── backend/           # Node.js backend
│   ├── config/       # Configuration files
│   ├── controllers/  # Route controllers
│   ├── middleware/   # Custom middleware
│   ├── models/       # Database models
│   ├── routes/       # API routes
│   └── server.js     # Entry point
└── README.md
```

