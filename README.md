Here’s an updated version of the README file with emojis and Cloudinary removed:

---

# 🌟 Social Flare - Server

![Social Flare Logo](https://via.placeholder.com/150)  
*A MERN Stack Social Media Platform*

## 🚀 Overview

This repository contains the backend code for **Social Flare**, a social media platform built using the MERN (MongoDB, Express, React, Node.js) stack. The backend handles all API requests, user authentication, database interactions, and features like user posts, likes, comments, and follows.

The client-side code can be found in the corresponding repository: [Social Flare Client](https://github.com/0127aryan/Social-Flare-Client).

## ✨ Features

- 🔑 **User Authentication**: Secure login and registration using JWT.
- 👤 **User Profiles**: Manage user profiles, followers, and following lists.
- 📝 **Posts Management**: Create, update, delete, and fetch posts.
- ❤️ **Likes and Comments**: Like and comment on posts.
- 👥 **Following System**: Follow/unfollow users to customize your feed.
- 📡 **RESTful API**: A well-structured set of API endpoints for frontend communication.

## 🛠️ Technologies Used

- **Node.js**: Runtime environment
- **Express.js**: Web framework for building the API
- **MongoDB**: NoSQL database for data storage
- **Mongoose**: ODM for MongoDB
- **JWT**: For secure user authentication
- **Multer**: For handling file uploads

## ⚙️ Installation and Setup

Follow these steps to set up the project on your local machine:

### 📋 Prerequisites

- **Node.js**: Download it [here](https://nodejs.org/).
- **npm** or **yarn**: Package manager to install dependencies.
- **MongoDB**: A MongoDB instance either locally or through [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).

### 📦 Clone the Repository

```bash
git clone https://github.com/0127aryan/Social-flare-server.git
cd Social-flare-server
```

### 📂 Install Dependencies

```bash
npm install
```

### 🔑 Environment Variables

Create a `.env` file in the root directory with the following values:

```bash
PORT=5000
MONGO_URI=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
```

Replace the placeholders with your actual credentials.

### ▶️ Running the Server

```bash
npm start
```

The server will start at `http://localhost:5000`.

## 🛣️ API Endpoints

Here are some of the key API endpoints:

- **Auth Routes**:
  - `POST /api/auth/register`: Register a new user
  - `POST /api/auth/login`: Log in a user

- **User Routes**:
  - `GET /api/users/:id`: Get user profile by ID
  - `PUT /api/users/:id`: Update user profile
  - `PUT /api/users/:id/follow`: Follow a user
  - `PUT /api/users/:id/unfollow`: Unfollow a user

- **Post Routes**:
  - `POST /api/posts`: Create a new post
  - `GET /api/posts/:id`: Get post by ID
  - `DELETE /api/posts/:id`: Delete post by ID
  - `PUT /api/posts/:id/like`: Like/unlike a post
  - `POST /api/posts/:id/comment`: Comment on a post

## 📁 Folder Structure

```
Social-flare-server/
├── config/                # Configuration files (MongoDB)
├── controllers/           # Logic for API routes
├── models/                # Mongoose models for Users, Posts, etc.
├── routes/                # API routes for Auth, Users, Posts
├── middlewares/           # Custom middlewares (Auth, Error handling)
├── utils/                 # Utility functions
├── .env                   # Environment variables
├── server.js              # Application entry point
├── package.json           # Project metadata and dependencies
└── README.md              # Project documentation
```

## ☁️ Deployment

Deploy the backend to services like **Heroku**, **Render**, or **Vercel**.

### Heroku Deployment Steps

1. Log in to Heroku and create a new app.
2. Run the following commands:

```bash
heroku login
heroku create social-flare-server
git push heroku main
heroku config:set MONGO_URI=<your_mongodb_connection_string>
heroku config:set JWT_SECRET=<your_jwt_secret>
```

## 🤝 Contributing

We welcome contributions! To get started:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a Pull Request.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

