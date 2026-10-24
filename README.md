# Task Management System

A MERN stack project for managing tasks with authentication, protected task APIs, and a responsive dashboard.

## Project Structure

- `server/` - Express backend with MongoDB and JWT auth
- `client/` - React + Vite frontend

## Milestones

1. Project setup
2. Backend and MongoDB connection
3. User authentication
4. Task management APIs
5. React frontend
6. Frontend-backend integration
7. Validation and testing
8. GitHub setup
9. Deployment
10. Submission documentation and screenshots

## Local setup

```bash
# Backend
cd server
npm install
cp .env.example .env
npm run dev

# Frontend
cd ../client
npm install
cp ../.env.example .env.local
npm run dev
```

## Notes

- Do not commit real `.env` files.
- Use MongoDB Atlas and JWT secrets in environment variables.
- Never expose credentials in code or in Git history.
