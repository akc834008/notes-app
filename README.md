# Notes Application

A secure **Notes Application** that allows users to create, read, update, and delete personal notes using **JWT (JSON Web Token) authentication**. Each user can access only their own notes after successful authentication.

---

## 🚀 Features

* User Registration & Login
* JWT-based Authentication & Authorization
* Create, Read, Update, Delete (CRUD) Notes
* Protected Routes (only authenticated users can access notes)
* Secure password hashing
* RESTful API architecture

---

## 🛠️ Tech Stack

* **Backend:** Node.js, Express.js
* **Database:** MongoDB (Mongoose ODM)
* **Authentication:** JWT (JSON Web Token)
* **Security:** bcrypt for password hashing
* **API Testing:** Postman / Thunder Client

---

## 📂 Project Structure

```
notes-app/
│── controllers/
│   ├── authController.js
│   └── noteController.js
│── models/
│   ├── User.js
│   └── Note.js
│── routes/
│   ├── authRoutes.js
│   └── noteRoutes.js
│── middleware/
│   └── authMiddleware.js
│── config/
│   └── db.js
│── .env
│── server.js
│── package.json
```

---

## 🔐 Authentication Flow (JWT)

1. User registers with email and password
2. Password is hashed using bcrypt and stored securely
3. User logs in with valid credentials
4. Server generates a JWT token
5. Token is sent to the client
6. Client sends token in the `Authorization` header for protected routes

```
Authorization: Bearer <JWT_TOKEN>
```

---

## 📌 API Endpoints

### Auth Routes

| Method | Endpoint           | Description            |
| ------ | ------------------ | ---------------------- |
| POST   | /api/auth/register | Register new user      |
| POST   | /api/auth/login    | Login user & get token |

### Notes Routes (Protected)

| Method | Endpoint       | Description        |
| ------ | -------------- | ------------------ |
| POST   | /api/notes     | Create a new note  |
| GET    | /api/notes     | Get all user notes |
| GET    | /api/notes/:id | Get note by ID     |
| PUT    | /api/notes/:id | Update note        |
| DELETE | /api/notes/:id | Delete note        |

---

## ⚙️ Environment Variables

Create a `.env` file in the root directory and add:

```
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
```

---

## ▶️ Installation & Setup

1. Clone the repository

```
git cl
```
