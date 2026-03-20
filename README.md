# 📝 Task Manager Application

A full-stack Task Manager application with secure authentication and complete CRUD functionality.

This project includes:

* Backend API (Node.js + TypeScript + Prisma + PostgreSQL)
* Frontend Web App (Next.js + TypeScript)

---

# 🚀 Features

## 🔐 Authentication

* User Registration
* User Login
* JWT Authentication (Access Token + Refresh Token)
* Secure password hashing using bcrypt
* Logout functionality

---

## 📝 Task Management

* Create new tasks
* View all tasks
* Update task title
* Delete tasks
* Toggle task status (Pending / Completed)

---

## 🎯 Additional Features

* Protected routes
* Clean UI with responsive design
* Token-based authorization
* Error handling with proper status codes

---

# 🏗️ Project Structure

```
task-manager/
│
├── task-manager-api/     # Backend (Node.js + Prisma)
│
└── task-frontend/        # Frontend (Next.js)
```

---

# ⚙️ Tech Stack

## Backend:

* Node.js
* TypeScript
* Express.js
* Prisma ORM
* PostgreSQL
* JWT (jsonwebtoken)
* bcrypt

## Frontend:

* Next.js (App Router)
* TypeScript
* Tailwind CSS
* Axios

---

# 🔄 Workflow of the Project

## 1. Authentication Flow

1. User registers using email & password
2. Password is hashed using bcrypt
3. User logs in → server generates:

   * Access Token (short-lived)
   * Refresh Token (long-lived)
4. Access Token is used for API requests
5. Refresh Token is used to generate new access tokens

---

## 2. Task Flow

1. User logs in
2. Access token is stored in frontend (localStorage)
3. All task APIs require Authorization header:

```
Authorization: Bearer <token>
```

4. User can:

   * Add task → POST /tasks
   * Get tasks → GET /tasks
   * Update → PATCH /tasks/:id
   * Delete → DELETE /tasks/:id
   * Toggle → PATCH /tasks/:id/toggle

---

## 3. Database Flow

* PostgreSQL database stores:

  * Users
  * Tasks
* Prisma ORM handles all database operations

---

# 🛠️ Setup Instructions

## 🔹 Backend Setup

```bash
cd task-manager-api
npm install
```

### Create `.env` file:

```
DATABASE_URL=postgresql://postgres:password@localhost:5432/taskdb
JWT_SECRET=your_secret
JWT_REFRESH_SECRET=your_refresh_secret
```

### Run migrations:

```bash
npx prisma generate
npx prisma db push
```

### Start backend:

```bash
npm run dev
```

---

## 🔹 Frontend Setup

```bash
cd task-frontend
npm install
npm run dev
```

---

# 🌐 API Endpoints

## Auth:

* POST /auth/register
* POST /auth/login
* POST /auth/refresh
* POST /auth/logout

## Tasks:

* GET /tasks
* POST /tasks
* PATCH /tasks/:id
* DELETE /tasks/:id
* PATCH /tasks/:id/toggle

---

# 🎯 Future Improvements

* Pagination support
* Search & filtering
* Mobile app (Flutter)
* Dark mode UI
* Deployment (Vercel + Render)

---

# 🏆 Conclusion

This project demonstrates:

* Full-stack development
* Secure authentication
* REST API design
* Database management
* Modern frontend UI

---

# 👨‍💻 Author 

Developed as part of a full-stack assignment.

 ---

 # Frontend UI

 
<img width="377" height="278" alt="image" src="https://github.com/user-attachments/assets/4c905950-62f3-4824-a00b-932523142b72" />
<img width="411" height="379" alt="image" src="https://github.com/user-attachments/assets/7b1b1469-d8f5-4086-8bd1-2c54af71b464" />
<img width="412" height="275" alt="image" src="https://github.com/user-attachments/assets/07e1ac07-883b-4f33-ad5e-91901bdcd623" />
<img width="361" height="272" alt="image" src="https://github.com/user-attachments/assets/6da24b33-00d3-4c8e-8f6e-c83c64723222" />



