# 📝 MyBlog

A full-stack blogging platform built with **React**, **Node.js/Express**, and **MongoDB**.  
Users can browse posts publicly, register/login to create and edit posts, and engage with comments.  
Includes authentication, protected routes, categories, and a personalized dashboard.

---

## 🚀 Features

- **Public browsing**
  - View all posts
  - Read individual posts
  - Browse posts by category
- **Authentication**
  - Register and login with JWT
  - Protected routes for creating, editing, and profile access
- **Dashboard**
  - Personalized landing page after login
  - Quick links to create or view posts
- **Posts**
  - Create, edit, delete posts
  - Slug-based URLs
  - Category assignment
- **Comments**
  - View comments publicly
  - Add comments when logged in
- **Profile**
  - View your own posts
  - Edit or delete posts from profile
- **UI**
  - Responsive design with TailwindCSS
  - Styled navbar with gradient background
  - Card layout for posts

---

## 🛠 Tech Stack

| Layer      | Technology                                  |
|------------|---------------------------------------------|
| Frontend   | React, React Router, Axios, TailwindCSS     |
| Backend    | Node.js, Express                            |
| Database   | MongoDB, Mongoose                          |
| Authentication | JWT, bcrypt                            |
| Deployment | Vercel (frontend), Render/Heroku (backend), MongoDB Atlas |

---

## 📂 Project Structure

```
myblog/
├── backend/
│ ├── models/ # Mongoose schemas (User, Post, Comment)
│ ├── routes/ # Express routes
│ ├── controllers/ # Business logic
│ └── server.js # Entry point
├── frontend/
│ ├── src/
│ │ ├── api/ # Axios API helpers
│ │ ├── components/ # Navbar, ProtectedRoute, PostList
│ │ ├── context/ # AuthContext
│ │ ├── pages/ # Home, AllPosts, PostDetail, CreateEditPage, Profile, Dashboard, Login, Register
│ │ └── App.jsx # Routes
└── README.md
```
text

---

## ⚙️ Installation & Setup

### 1. Clone the repo
git clone https://github.com/yourusername/myblog.git
cd myblog

text

### 2. Backend setup
cd backend
npm install

text

Create a `.env` file in `backend/` with:
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

text

Run the backend:
npm run dev

text

### 3. Frontend setup
cd ../frontend
npm install

text

Create `.env` file in `frontend/` with:
VITE_API_URL=http://localhost:5000/api

text

Run frontend:
npm run dev

text

---

## 🔑 API Endpoints

- **Auth**
  - `POST /api/auth/register` → Register new user
  - `POST /api/auth/login` → Login user
- **Posts**
  - `GET /api/posts` → Get all posts
  - `GET /api/posts/:slug` → Get single post
  - `POST /api/posts` → Create post (auth required)
  - `PUT /api/posts/:slug` → Update post (auth required)
  - `DELETE /api/posts/:slug` → Delete post (auth required)
  - `GET /api/posts/user/me` → Get logged-in user’s posts
  - `GET /api/posts/category/:category` → Get posts by category
- **Comments**
  - `GET /api/comments/:postId` → Get comments for post
  - `POST /api/comments/:postId` → Add comment (auth required)

---

## 🎨 Screenshots

- Home Page: Recent posts preview
- All Posts: Grid of posts with category filter
- Post Detail: Full post + comments
- Dashboard: Welcome message + quick links
- Profile: User’s posts with edit/delete actions

---

## 📌 Future Improvements

- Rich text editor for posts
- Image upload for cover photos
- Pagination & search
- Dynamic category management
- Like system for posts/comments

---

## 👨‍💻 Author

Developed by Haruna Ademoye. Feel free to contribute or fork the project!

---
