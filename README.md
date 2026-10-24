# TaskFlow — Task Management System

A full-stack MERN (MongoDB, Express, React, Node.js) task management application built for capstone use. This project allows users to register, log in, create, update, delete, search, and filter tasks in a clean dashboard interface.

Project repository: https://github.com/Eliz2132/task-management-system

## Project Overview

TaskFlow is designed to help users organize tasks efficiently by providing:
- secure user authentication
- protected task APIs
- dashboard-based task tracking
- status and priority management
- quick search and filtering
- responsive UI for desktop and mobile

## Capstone Objective

The goal of this project is to build a complete full-stack web application that demonstrates practical software engineering skills, including:
- frontend development with React
- backend API development with Express and Node.js
- database modeling with MongoDB and Mongoose
- authentication and authorization with JWT
- environment configuration and deployment preparation
- GitHub project management and documentation

## Features

### User Features
- User registration
- User login
- JWT-based protected routes
- Logout functionality
- User profile display in the navbar

### Task Features
- Create new tasks
- View all tasks in a dashboard
- Edit existing tasks
- Delete tasks
- Track task status:
  - To do
  - In progress
  - Completed
- Track task priority:
  - Low
  - Medium
  - High
- Due date support
- Search by task title or keyword
- Filter by status and priority
- Empty state when no task matches the active filters

### UI/UX Features
- Responsive dashboard layout
- Card-based task presentation
- Clean modern styling
- Mobile-friendly design
- Loading and error states

## Tech Stack

### Frontend
- React
- Vite
- React Router DOM
- Axios

### Backend
- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- bcryptjs

### Tools
- GitHub for version control
- MongoDB Atlas for cloud database
- Vercel for frontend deployment
- Render for backend deployment

## Project Structure

```text
task-management-system/
├── client/                 # React frontend
│   ├── src/
│   ├── package.json
│   └── vite.config.js
├── server/                 # Express backend
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── .env.example
│   ├── package.json
│   └── server.js
├── README.md
└── .gitignore
```

## Local Setup

### 1. Clone the repository

```bash
git clone https://github.com/Eliz2132/task-management-system.git
cd task-management-system
```

### 2. Setup backend

```bash
cd server
npm install
cp .env.example .env
```

If you are using PowerShell on Windows:

```powershell
Copy-Item .env.example .env
```

### 3. Configure environment variables

Open `server/.env` and update the values:

```env
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/taskmanagement
JWT_SECRET=your_secret_key_here
```

Example:

```env
PORT=5000
MONGO_URI=mongodb+srv://myuser:mypassword@cluster0.abcde.mongodb.net/taskmanagement
JWT_SECRET=my_super_secret_jwt_key_2026
```

### 4. Start backend

```bash
npm run dev
```

### 5. Setup frontend

Open a new terminal tab:

```bash
cd client
npm install
npm run dev
```

### 6. Open the app

Visit:

```text
http://localhost:5173
```

## Environment Variables

### Backend (`server/.env`)
| Variable | Description |
|---|---|
| PORT | Port used by the Express server |
| MONGO_URI | MongoDB connection string |
| JWT_SECRET | Secret key for token generation |

## API Overview

### Authentication
- `POST /api/auth/register` — create a new user
- `POST /api/auth/login` — authenticate a user and return a JWT

### Tasks
- `GET /api/tasks` — fetch tasks for the logged-in user
- `POST /api/tasks` — create a new task
- `PUT /api/tasks/:id` — update a task
- `DELETE /api/tasks/:id` — delete a task

## Deployment Plan

This project is ready for deployment using a common MERN deployment setup.

### Recommended Deployment Architecture

#### Frontend
- Host on Vercel
- Connect the `client` app to Vercel
- Set environment variables for API base URL if needed

#### Backend
- Host on Render
- Deploy the Express server from the `server` directory
- Set environment variables:
  - `PORT`
  - `MONGO_URI`
  - `JWT_SECRET`

#### Database
- Use MongoDB Atlas
- Create a free/shared cluster
- Whitelist IP addresses or allow access from anywhere depending on hosting setup

### Deployment Steps

1. Create a MongoDB Atlas cluster.
2. Get the connection string and save it in the backend environment variables.
3. Create a Render service for the backend.
4. Add the required environment variables in Render.
5. Deploy the backend and note the live API URL.
6. Create a Vercel project for the frontend.
7. Set the frontend API base URL to the deployed backend URL.
8. Build and deploy the frontend.
9. Test login, registration, and task CRUD workflow on the deployed app.
10. Update README with the final live demo link.

### Example Production Configuration

Frontend environment variable (if used):
```env
VITE_API_URL=https://your-render-app.onrender.com/api
```

Backend environment variables on Render:
```env
PORT=5000
MONGO_URI=mongodb+srv://username:password@cluster.mongodb.net/taskmanagement
JWT_SECRET=your_secure_secret_key
```

## Deployment Status

Current local app is ready for development.

Live deployment URL: To be added after hosting is completed.

## Demo / Screenshots

Add screenshots here once the app is running locally or deployed:
- Login page
- Registration page
- Dashboard
- Task creation form
- Search and filter demo

## Security Notes

- Never expose `.env` files in GitHub
- Store secret keys securely
- Use JWT for authenticated API access
- Restrict database credentials and API access appropriately
- Do not commit production secrets or real credentials

## GitHub Workflow

Suggested project workflow:
- main branch for stable code
- feature branches for new work
- commit changes with clear messages
- use pull requests before merging major features

## Future Improvements

Possible enhancements for future versions:
- drag-and-drop task organization
- task sorting by due date or priority
- dark mode
- team collaboration and shared boards
- notifications and reminders
- analytics dashboard
- deployment automation with CI/CD

## Conclusion

TaskFlow demonstrates a complete MERN stack application with secure authentication and task management features. It is suitable for a capstone project because it combines frontend, backend, database, and deployment knowledge in one practical application.

## Credits

Developed as a MERN stack capstone project.

## License

This project is for academic/capstone use and can be adapted for personal or educational projects.

---

If you want, this README can also be customized further with:
- your name and student ID
- project title branding
- screenshot placeholders
- a final live deployment URL
- a more formal academic capstone format
