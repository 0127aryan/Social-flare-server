Here’s a README file for your **Social Flare Server** repository:

---

# Social Flare - Server

![Social Flare Logo](https://via.placeholder.com/150)  
*A MERN Stack Social Media Platform*

## Overview

This repository contains the backend code for **Social Flare**, a social media platform built using the MERN (MongoDB, Express, React, Node.js) stack. The backend is responsible for handling all API requests, user authentication, database interactions, and managing user posts, likes, comments, and follows.

The client-side code can be found in the corresponding repository: [Social Flare Client](https://github.com/0127aryan/Social-Flare-Client).

## Features

- **User Authentication**: Implements JWT-based authentication for secure login and sign-up.
- **User Profiles**: Manage user profiles, including followers and following lists.
- **Posts Management**: Create, update, delete, and fetch posts for users.
- **Likes and Comments**: Functionality for liking and commenting on posts.
- **Following System**: Users can follow/unfollow others and see posts in their feed accordingly.
- **RESTful API**: Provides a set of API endpoints for interaction with the frontend.

## Technologies Used

- **Node.js**: Runtime environment
- **Express.js**: Web framework for building the API
- **MongoDB**: Database for storing user and post information
- **Mongoose**: ODM for MongoDB
- **JWT**: For user authentication
- **Cloudinary**: For image uploads and storage
- **Multer**: For handling file uploads

## Installation and Setup

Follow the steps below to run the project on your local machine:

### Prerequisites

- **Node.js**: Make sure you have Node.js installed. You can download it [here](https://nodejs.org/).
- **npm** or **yarn**: A package manager for installing dependencies.
- **MongoDB**: You need a MongoDB instance. You can set it up locally or use [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).

### Clone the Repository

```bash
git clone https://github.com/0127aryan/Social-flare-server.git
cd Social-flare-server
```

### Install Dependencies

Run the following command to install all necessary dependencies:

```bash
npm install
```

### Environment Variables

Create a `.env` file in the root directory and add the following environment variables:

```bash
PORT=5000
MONGO_URI=<your_mongodb_connection_string>
JWT_SECRET=<your_jwt_secret>
CLOUDINARY_CLOUD_NAME=<your_cloudinary_cloud_name>
CLOUDINARY_API_KEY=<your_cloudinary_api_key>
CLOUDINARY_API_SECRET=<your_cloudinary_api_secret>
```

Replace the placeholders with your actual credentials:

- `<your_mongodb_connection_string>`: Your MongoDB URI
- `<your_jwt_secret>`: A secret string for JWT signing
- `<your_cloudinary_cloud_name>`, `<your_cloudinary_api_key>`, `<your_cloudinary_api_secret>`: Cloudinary credentials for image storage.

### Running the Server

To start the server, run:

```bash
npm start
```

The server will run on `http://localhost:5000` by default.

### API Endpoints

Here are some of the main API endpoints:

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

## Folder Structure

```
Social-flare-server/
├── config/                # Configuration files (MongoDB, Cloudinary)
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

## Deployment

The backend can be deployed on platforms like **Heroku**, **Render**, or **Vercel**.

### Heroku Deployment

1. Set up a Heroku account and install the Heroku CLI.
2. Run the following commands to deploy:
   
```bash
heroku login
heroku create social-flare-server
git push heroku main
heroku config:set MONGO_URI=<your_mongodb_connection_string>
heroku config:set JWT_SECRET=<your_jwt_secret>
heroku config:set CLOUDINARY_CLOUD_NAME=<your_cloudinary_cloud_name>
heroku config:set CLOUDINARY_API_KEY=<your_cloudinary_api_key>
heroku config:set CLOUDINARY_API_SECRET=<your_cloudinary_api_secret>
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Let me know if you'd like any changes or additions!
