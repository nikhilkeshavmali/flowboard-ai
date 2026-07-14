# 🚀 FlowBoard

> **AI-Powered Kanban Board with Real-Time Collaboration**

FlowBoard is a modern full-stack project management application that helps teams organize work efficiently using Kanban boards. It combines real-time collaboration with AI-powered productivity features, allowing users to create boards, manage tasks, collaborate with team members, and generate intelligent task suggestions using **Google Gemini AI**.

---

## ✨ Features

### 🔐 Authentication & Security
- User Registration & Login
- JWT-based Authentication
- Password Hashing using bcrypt
- Protected API Routes

### 📋 Board Management
- Create, Update & Delete Boards
- Custom Board Colors
- Default Kanban Columns
- Board Activity History

### ✅ Task Management
- Create, Update & Delete Tasks
- Drag & Drop Task Movement
- Task Priorities
- Due Dates
- Task Assignment
- Task Filtering & Search

### 👥 Team Collaboration
- Invite Members via Email
- Owner/Admin Roles
- Board Access Control
- Real-Time Presence

### ⚡ Real-Time Features
- Live Task Updates
- Live Board Updates
- Activity Feed
- Socket.IO Integration

### 🤖 AI Features (Google Gemini)
- Generate Tasks from Project Goals
- Break Large Tasks into Subtasks
- Generate Sprint/Board Summary
- AI-Powered Productivity Assistance

---

# 🛠️ Tech Stack

## Frontend

- React.js
- Vite
- JavaScript (ES6+)
- Tailwind CSS
- Axios
- React Router
- Socket.IO Client

## Backend

- Node.js
- Express.js
- PostgreSQL
- Socket.IO
- JWT Authentication
- bcryptjs
- Google Gemini AI
- dotenv

---

# 📂 Project Structure

```text
FlowBoard/
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── .env.example
│
├── backend/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── middleware/
│   │   ├── routes/
│   │   ├── services/
│   │   ├── realtime/
│   │   ├── socket/
│   │   └── utils/
│   │
│   ├── schema.sql
│   ├── package.json
│   └── .env.example
│
├── README.md
└── .gitignore
```

---

# ⚙️ Installation

## Clone Repository

```bash
git clone https://github.com/yourusername/flowboard-ai.git

cd flowboard-ai
```

---

# Backend Setup

```bash
cd backend

npm install
```

Create `.env`

```env
PORT=5050

DATABASE_URL=your_postgresql_database_url

JWT_SECRET=your_secret_key

JWT_EXPIRES_IN=7d

CLIENT_URL=http://localhost:5173

GEMINI_API_KEY=your_gemini_api_key

GEMINI_MODEL=gemini-2.0-flash
```

Run Database Schema

```bash
npm run migrate
```

Start Backend

```bash
npm run dev
```

Backend runs at

```
http://localhost:5050
```

---

# Frontend Setup

```bash
cd frontend

npm install
```

Create `.env`

```env
VITE_API_URL=http://localhost:5050/api

VITE_SOCKET_URL=http://localhost:5050
```

Start Frontend

```bash
npm run dev
```

Frontend runs at

```
http://localhost:5173
```

---

# Database

FlowBoard uses **PostgreSQL**.

Tables include:

- users
- boards
- board_members
- columns
- tasks
- activities

---

# REST API

## Authentication

```
POST   /api/auth/register

POST   /api/auth/login

GET    /api/auth/me
```

---

## Boards

```
GET     /api/boards

POST    /api/boards

GET     /api/boards/:boardId

PATCH   /api/boards/:boardId

DELETE  /api/boards/:boardId
```

---

## Tasks

```
GET     /api/boards/:boardId/tasks

POST    /api/boards/:boardId/tasks

PATCH   /api/boards/:boardId/tasks/:taskId

PATCH   /api/boards/:boardId/tasks/:taskId/move

DELETE  /api/boards/:boardId/tasks/:taskId
```

---

## AI

```
POST /api/boards/:boardId/ai/generate-tasks

POST /api/boards/:boardId/ai/breakdown

POST /api/boards/:boardId/ai/summary
```

---

# Socket.IO Events

### Client

- board:join
- board:leave
- presence:cursor

### Server

- task:created
- task:updated
- task:moved
- task:deleted
- board:updated
- board:deleted
- activity:new
- presence:join
- presence:leave

---

# Future Improvements

- Notifications
- File Attachments
- Comments
- Dark Mode
- Calendar View
- Labels
- Checklists
- Email Invitations
- Mobile Responsive Enhancements

---

# Screenshots

Add screenshots here.

# 📸 Screenshots

## 🏠 Home Page

<img width="100%" alt="Home Page" src="https://github.com/user-attachments/assets/604ee164-5050-479d-bc83-830957184b17" />

---

## 📋 Board Dashboard

<img width="100%" alt="Board Dashboard" src="https://github.com/user-attachments/assets/b58281a1-0573-4b9d-96cd-2df9718bace2" />

---

## ✅ Task Management

<img width="100%" alt="Task Management" src="https://github.com/user-attachments/assets/4214f0af-a262-4fa5-8873-c48cbf7505f7" />

---

## 🤖 AI Task Generation

<img width="100%" alt="AI Task Generation" src="https://github.com/user-attachments/assets/c6a58d33-e1c5-477a-ad52-321a8e5e65ba" />

---

# Environment Variables

## Backend

```env
PORT=
DATABASE_URL=
JWT_SECRET=
JWT_EXPIRES_IN=
CLIENT_URL=
GEMINI_API_KEY=
GEMINI_MODEL=
```

## Frontend

```env
VITE_API_URL=
VITE_SOCKET_URL=
```

---

# Author

**Nikhil Mali**

GitHub: https://github.com/nikhilkeshavmali

LinkedIn: https://www.linkedin.com/in/nikhilkeshavmali

Portfolio: https://nikhil-portfolio-bay.vercel.app/

---

## ⭐ If you like this project, don't forget to give it a Star!
