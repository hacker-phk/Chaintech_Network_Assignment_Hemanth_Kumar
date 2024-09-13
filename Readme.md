Here’s an advanced README template that you can use for your **Node.js To-Do List** project connected to MongoDB Atlas. This template includes icons, clear sections, and proper documentation language to make your project stand out.

---

# 📝 Node.js To-Do List API with MongoDB Atlas

[![Node.js](https://img.shields.io/badge/Node.js-v14+-green.svg?style=flat&logo=node.js)](https://nodejs.org/)
[![Express.js](https://img.shields.io/badge/Express.js-4.x-black.svg?style=flat&logo=express)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-green.svg?style=flat&logo=mongodb)](https://www.mongodb.com/cloud/atlas)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

This project is a RESTful API for managing a **To-Do List** built with **Node.js**, **Express**, and **MongoDB Atlas**. Users can create, read, update, and delete tasks, with features like task completion, task categorization, and due dates.

## 🚀 Features

- 📝 **Create tasks** with titles and descriptions
- 🔍 **View all tasks** stored in the database
- ✏️ **Edit task details** (title, description, completion status)
- ✅ **Mark tasks as completed**
- ❌ **Delete tasks** from the list
- 📅 **Optional**: Add task due dates and categories

---

## 🛠️ Installation

Follow these instructions to set up and run the project on your local machine.

### Prerequisites

- **Node.js** (v14+ recommended) – [Install here](https://nodejs.org/)
- **MongoDB Atlas** account – [Set up MongoDB Atlas](https://www.mongodb.com/cloud/atlas)

### Clone the Repository

```bash
git clone https://github.com/yourusername/todo-app.git
cd todo-app
```

### Install Dependencies

```bash
npm install
```

### Set up Environment Variables

1. Create a `.env` file in the root of your project directory.
2. Add your MongoDB Atlas URI to the `.env` file:

```bash
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/<dbname>?retryWrites=true&w=majority
```

### Run the Application

Start the server:

```bash
npm start
```

The server will run on `http://localhost:5000`.

---

## 🗂️ API Documentation

The API provides several endpoints for managing tasks. Here’s a detailed overview of each route.

### Base URL

```
http://localhost:5000/tasks
```

### 📌 Endpoints

#### 1. **Create a Task**
```http
POST /tasks
```
- **Request Body:**
  ```json
  {
    "title": "Buy Groceries",
    "description": "Milk, Bread, Eggs"
  }
  ```
- **Response:**
  ```json
  {
    "message": "Task created successfully",
    "task": {
      "_id": "613b4f0f4a9c4e001e3d3cfb",
      "title": "Buy Groceries",
      "description": "Milk, Bread, Eggs",
      "completed": false,
      "createdAt": "2023-09-10T10:10:10.123Z"
    }
  }
  ```

#### 2. **Get All Tasks**
```http
GET /tasks
```
- **Response:**
  ```json
  [
    {
      "_id": "613b4f0f4a9c4e001e3d3cfb",
      "title": "Buy Groceries",
      "description": "Milk, Bread, Eggs",
      "completed": false,
      "createdAt": "2023-09-10T10:10:10.123Z"
    },
    ...
  ]
  ```

#### 3. **Update a Task**
```http
PUT /tasks/:id
```
- **Request Body:**
  ```json
  {
    "title": "Go Jogging",
    "description": "Morning jog",
    "completed": true
  }
  ```
- **Response:**
  ```json
  {
    "message": "Task updated successfully",
    "task": {
      "_id": "613b4f0f4a9c4e001e3d3cfb",
      "title": "Go Jogging",
      "description": "Morning jog",
      "completed": true
    }
  }
  ```

#### 4. **Delete a Task**
```http
DELETE /tasks/:id
```
- **Response:**
  ```json
  {
    "message": "Task deleted successfully"
  }
  ```

#### 5. **Mark a Task as Completed**
```http
PATCH /tasks/:id/completed
```
- **Response:**
  ```json
  {
    "message": "Task marked as completed",
    "task": {
      "_id": "613b4f0f4a9c4e001e3d3cfb",
      "title": "Go Jogging",
      "description": "Morning jog",
      "completed": true
    }
  }
  ```

---



## 🔧 Project Structure

```
todo-app/
│
├── models/
│   └── Task.js              # Mongoose schema for tasks
│
├── routes/
│   └── taskRoutes.js        # API routes for task management
│
├── app.js                   # Main application file
├── .env                     # Environment variables (not pushed to GitHub)
├── package.json             # Project metadata and dependencies
├── README.md                # Project documentation
└── tests/                   # Unit tests (optional)
```

---

## 📚 Learning Resources

To help you get started with Node.js and MongoDB, here are some recommended resources:

- [Node.js Official Documentation](https://nodejs.org/en/docs/)
- [Express.js Documentation](https://expressjs.com/)
- [MongoDB Atlas Documentation](https://docs.atlas.mongodb.com/)
- [Mongoose Documentation](https://mongoosejs.com/)

---


## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 👤 Author

- GitHub: [hacker-phk](https://github.com/hacker-phk)
- LinkedIn: [hemanthkumarpujari](https://www.linkedin.com/in/hemanthkumarpujari/)

---

Feel free to modify this README as necessary to reflect your specific project details. Let me know if you need help with any other part of your project!