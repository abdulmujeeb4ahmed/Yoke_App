# Yoke App Backend

This repository contains the backend server for the Yoke App, built with Node.js, Express, and MongoDB.

## 🚀 Getting Started

Follow these steps to set up and run the server on your local machine.

## 📌 Prerequisites

Ensure you have the following installed:

- **Node.js** (v18 or later recommended)
- **MongoDB Atlas** (or a local MongoDB instance)
- **Postman** (optional for API testing)

## 📥 Installation

### 1️⃣ Clone the Repository

```sh
git clone https://github.com/abdulmujeeb4ahmed/Yoke_App
cd yoke-app
```

### 2️⃣ Install Dependencies

```sh
npm install
```

### 3️⃣ Configure Environment Variables

Create a `.env` file in the root directory and add your MongoDB connection string:

```env
MONGO_URI=mongodb+srv://your_username:your_password@your-cluster.mongodb.net/?retryWrites=true&w=majority&appName=YokeAWS-Cluster
PORT=5002
```

⚠️ **Important:** Replace `your_username`, `your_password`, and `your-cluster` with actual values from your MongoDB Atlas setup. The username is your GitHub username and the password is the long password I sent on Slack to each of you privately.

### 4️⃣ Start the Server

```sh
node index.js
```

If successful, you should see:

```
🚀 Server running on port 5002
✅ Connected to MongoDB
```

## 🛠 API Endpoints

### 📌 User Routes

| Method | Endpoint           | Description          |
|--------|-------------------|----------------------|
| GET    | /api/users        | Get all users       |
| GET    | /api/users/:id    | Get user by ID      |
| POST   | /api/users        | Create a new user   |
| PUT    | /api/users/:id    | Update user by ID   |
| DELETE | /api/users/:id    | Delete user by ID   |

## 📌 Example API Request (Using Postman or Curl)

### ➤ Create a User

```http
POST http://localhost:5002/api/users
Content-Type: application/json

{
  "name": "John Doe",
  "email": "john@example.com"
}
```

### ➤ Get All Users

```http
GET http://localhost:5002/api/users
```

### ➤ Update a User

```http
PUT http://localhost:5002/api/users/:id
Content-Type: application/json

{
  "name": "Updated Name",
  "email": "updated@example.com"
}
```

### ➤ Delete a User

```http
DELETE http://localhost:5002/api/users/:id
```

## 🔥 Troubleshooting

- **Port Already in Use Error (EADDRINUSE):** Run the following command to find and kill the process using port 5002:

  ```sh
  lsof -i :5002
  kill -9 <PID>
  ```

- **MongoDB Connection Issues:** Ensure your `MONGO_URI` is correct and that your MongoDB Atlas database allows access from your IP address.

## 📜 License

This project is licensed under the **MIT License**.

## 🎯 Next Steps

- Implement authentication (JWT)
- Deploy to AWS/GCP
- Connect to a frontend

Now, you're all set! 🚀 Happy coding! 😃
