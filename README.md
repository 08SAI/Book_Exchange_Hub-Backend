
# 📚 Book Exchange Hub – Backend API

Welcome to the **Backend API** of **Book Exchange Hub** – a vibrant, community-powered platform where users can **list, discover, and exchange books** 📖🤝. This RESTful API is built with **Node.js**, **Express**, and **MongoDB**, providing the core functionality for user authentication, book management, and secure data handling.

---

## 🚀 Key Features

🔐 **Authentication & Security**
- JWT-based auth with secure HTTP-only cookies 🍪  
- User registration, login, and logout  
- Password reset via email (token-based recovery) ✉️

📚 **Book Management**
- Add, update, or remove books with ease  
- Get single or multiple books with pagination support  
- Smart search by title, genre, or author 🔎

🛡️ **Robust Middleware**
- Centralized error handling  
- Async handler for cleaner routes  
- Protected routes for authenticated users 🔒

🌍 **Other Goodies**
- CORS enabled for frontend-backend communication 🔁  
- Scalable project structure & environment support  

---

## 📁 Project Structure

```
📦 Book Exchange Hub Backend
├── package.json
├── server.js
├── config/
│   ├── config.env
│   └── db.js
├── controllers/
│   ├── auth.js
│   └── books.js
├── middleware/
│   ├── async.js
│   ├── auth.js
│   └── error.js
├── models/
│   ├── Book.js
│   └── User.js
├── routes/
│   ├── auth.js
│   └── book.js
└── utils/
    └── errorResponse.js
```

---

## 🧰 Getting Started

### ✅ Prerequisites

- ⚙️ Node.js (v14+)
- 🗃️ MongoDB (Atlas or local instance)

### 🔧 Installation

1. **Clone the Repository**
   ```bash
   git clone <repo-url>
   cd BOOK-EXCHANGE-HUB-BACKEND
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Configure Environment**
   - Add your variables to `config/config.env`

---

### 💻 Running the Server

#### 🛠️ Development Mode:
```bash
npm run dev
```

#### 🚀 Production Mode:
```bash
npm start
```

> Server runs on port defined in `.env` (default: `5000`)

---

## 🔗 API Endpoints

### 🔐 Auth Routes
- `POST /book-barter-platform/api/register` – Register a new user  
- `POST /book-barter-platform/api/login` – Login and receive token  
- `GET /book-barter-platform/api/getLoggedInUser` – Get current logged-in user *(Protected)*  
- `POST /book-barter-platform/api/forgotPassword` – Request password reset  
- `PUT /book-barter-platform/api/resetPassword/:resettoken` – Reset password via token  

### 📘 Book Routes
- `POST /book-barter-platform/api/addBook` – Add a new book  
- `GET /book-barter-platform/api/getBook/:id` – Get book details by ID  
- `GET /book-barter-platform/api/getBooks` – Fetch books with optional search/pagination  
- `PUT /book-barter-platform/api/updateBook/:id` – Update book info  
- `PUT /book-barter-platform/api/removeBook/:id` – Remove book from listings  

---

## ⚙️ Environment Variables

Your `.env` file (`config/config.env`) should include:

```env
NODE_ENV=development
PORT=5000
MONGO_URI=your_mongo_connection_string
JWT_SECRET=your_jwt_secret
JWT_EXPIRE=30d
JWT_COOKIE_EXPIRE=30
```

Optional (for email functionality):
```env
SMTP_HOST=
SMTP_PORT=
SMTP_EMAIL=
SMTP_PASSWORD=
FROM_NAME=
FROM_EMAIL=
```

---


## 🤝 Contributions & Questions

Feel free to open issues, suggest features, or contribute via PRs!  
Let’s build a more connected community of readers together 💬📚
