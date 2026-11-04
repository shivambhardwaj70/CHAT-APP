# 💬 CHAT-APP — Real-Time Chat Application

A full-stack real-time messaging application built using the **MERN stack and Socket.IO**, designed to make communication seamless through instant messaging, friend management, group conversations, and live user presence.

The application combines a responsive React frontend with a Node.js and Express backend, MongoDB for persistent data storage, and Socket.IO for real-time communication.

---

## ✨ Features

### 👤 User Authentication & Management
- User registration and login.
- JWT-based authentication.
- Secure HTTP-only cookie-based session handling.
- User profile and avatar support.
- Search for other users.

### 💬 Real-Time Messaging
- Instant message delivery using Socket.IO.
- One-to-one and group conversations.
- Persistent message storage with MongoDB.
- Real-time message notifications.
- Typing indicators.
- Live online/offline user status.

### 👥 Friends & Group Management
- Send and accept friend requests.
- Manage friend lists.
- View notifications and pending requests.
- Create new group conversations.
- Add or remove group members.
- Rename and leave groups.
- Delete group conversations.

### 📎 File Sharing
- Send message attachments.
- Cloudinary integration for media uploads.
- Support for different uploaded file types.

### 🛡️ Admin Dashboard
- Dedicated admin authentication.
- View registered users.
- Monitor conversations and messages.
- Access dashboard statistics.

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, Vite, JavaScript |
| UI | Material UI (MUI) |
| State Management | Redux Toolkit, React Redux |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Real-Time Communication | Socket.IO |
| Authentication | JWT, Cookie Parser, Bcrypt |
| File Storage | Cloudinary, Multer |
| API Communication | Axios |
| Data Visualization | Chart.js |

---

## 🏗️ Architecture

The application follows a client-server architecture.

**Frontend**
- Provides the user interface and application navigation.
- Manages application state using Redux Toolkit.
- Communicates with backend APIs using Axios.
- Establishes Socket.IO connections for real-time updates.

**Backend**
- Exposes REST APIs for authentication, users, chats, and administration.
- Handles authentication and authorization.
- Manages chat and message operations.
- Establishes real-time communication using Socket.IO.
- Stores application data in MongoDB.
- Handles media uploads through Cloudinary.

---

## 📂 Project Structure

```text
CHAT-APP/
│
├── chatApp_server/
│   ├── app.js
│   ├── routes_user.js
│   ├── routes_chat.js
│   ├── routes_admin.js
│   ├── package.json
│   └── ...
│
├── src/
│   └── ...                  # React application
│
├── public/
│
├── package.json             # Frontend dependencies
├── vite.config.js
├── index.html
└── README.md
```

---

## 🚀 Getting Started

Follow these steps to run the application locally.

### 1. Prerequisites

Make sure you have installed:

- Node.js
- npm
- MongoDB (local instance or MongoDB Atlas account)
- Cloudinary account

### 2. Clone the Repository

```bash
git clone https://github.com/shivambhardwaj70/CHAT-APP.git

cd CHAT-APP
```

### 3. Install Frontend Dependencies

From the project root:

```bash
npm install
```

### 4. Install Backend Dependencies

```bash
cd chatApp_server

npm install
```

### 5. Configure Environment Variables

Create a `.env` file inside the `chatApp_server` directory.

Add the following variables:

```env
PORT=3000
NODE_ENV=development

MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret
ADMIN_SECRET_KEY=your_admin_secret_key

CLIENT_URL=http://localhost:5173

CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

Replace the placeholder values with your actual credentials.

**Important:** Never commit your `.env` file or expose database credentials, JWT secrets, or Cloudinary API secrets publicly.

### 6. Start the Backend Server

From the `chatApp_server` directory:

```bash
npm run dev
```

The backend will start on the configured port (default: `3000`).

### 7. Start the Frontend

Open a separate terminal and navigate to the project root:

```bash
cd CHAT-APP

npm run dev
```

Open the local URL displayed by Vite, typically:

```text
http://localhost:5173
```

You should now be able to access the application locally.

---

## 🔌 API Overview

The backend exposes RESTful API routes organized into three main modules.

| Module | Base Route | Purpose |
|---|---|---|
| User | `/api/v1/user` | Registration, login, profiles, friends and notifications |
| Chat | `/api/v1/chat` | Conversations, groups, messages and attachments |
| Admin | `/api/v1/admin` | Admin authentication, users, chats and statistics |

Real-time communication is handled separately through Socket.IO events.

---

## ⚡ Real-Time Communication

Socket.IO enables instant communication between connected users.

Some of the implemented real-time events include:

- `NEW_MESSAGE` — Handles real-time message delivery.
- `NEW_MESSAGE_ALERT` — Notifies users about new messages.
- `START_TYPING` — Indicates that a user is typing.
- `STOP_TYPING` — Indicates that a user has stopped typing.
- `ONLINE_USERS` — Synchronizes online user information.
- `CHAT_JOINED` — Handles chat participation.
- `CHAT_LEAVED` — Handles chat departure.

These events help maintain synchronized conversations and live user activity.

---

## 🔐 Security Considerations

- JWT-based authentication.
- HTTP-only authentication cookies.
- Protected user and chat routes.
- Admin-only route authorization.
- Request validation using Express Validator.
- Environment-based configuration for sensitive credentials.

---

## 👨‍💻 Author

**Shivam Bhardwaj**

- GitHub: [@shivambhardwaj70](https://github.com/shivambhardwaj70)
- Project: [CHAT-APP](https://github.com/shivambhardwaj70/CHAT-APP)

---

*Built with a focus on full-stack development, real-time communication, and scalable application architecture.*
