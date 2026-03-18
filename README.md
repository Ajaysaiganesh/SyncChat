# 💬 SyncChat

A real-time full-stack chat application built with the MERN stack and Socket.io — featuring instant messaging, image sharing, online presence indicators, profile customization, and 32 UI themes.

🔗 **Live Demo:** [https://syncchat-h5is.onrender.com](https://syncchat-h5is.onrender.com)
---

## ✨ Features

- 🔐 **Authentication & Authorization** — Secure JWT-based auth with HTTP-only cookies
- 💬 **Real-Time Messaging** — Instant messaging powered by Socket.io
- 🖼️ **Image Sharing** — Send images in chat, uploaded via Cloudinary
- 🟢 **Online Presence** — See which users are currently online in real time
- 👤 **Profile Management** — Update profile picture with Cloudinary upload
- 🎨 **32 UI Themes** — Powered by DaisyUI with persistent theme selection
- 📱 **Responsive Design** — Works seamlessly on mobile, tablet, and desktop
- 🔔 **Toast Notifications** — Instant feedback for all user actions
- ⚡ **Optimistic UI** — Messages appear instantly with smooth scrolling

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| React 19 | UI Framework |
| Vite | Build Tool |
| Zustand | State Management |
| Socket.io Client | Real-Time Communication |
| TailwindCSS + DaisyUI | Styling & UI Components |
| React Router DOM | Client-Side Routing |
| Axios | HTTP Requests |
| React Hot Toast | Notifications |
| Lucide React | Icons |

### Backend
| Technology | Purpose |
|---|---|
| Node.js + Express 5 | Server Framework |
| MongoDB + Mongoose | Database |
| Socket.io | WebSocket Server |
| JWT | Authentication Tokens |
| bcryptjs | Password Hashing |
| Cloudinary | Image Storage |
| Cookie Parser | Cookie Handling |
| dotenv | Environment Variables |

---

## 📁 Project Structure

```
syncchat/
├── backend/
│   └── src/
│       ├── controllers/
│       │   ├── auth.controller.js      # Signup, login, logout, update profile
│       │   └── message.controller.js   # Get users, get messages, send message
│       ├── lib/
│       │   ├── cloudinary.js           # Cloudinary configuration
│       │   ├── db.js                   # MongoDB connection
│       │   ├── socket.js               # Socket.io server setup
│       │   └── utils.js                # JWT token generation
│       ├── middleware/
│       │   └── auth.middleware.js      # Protect routes middleware
│       ├── models/
│       │   ├── user.model.js           # User schema
│       │   └── message.model.js        # Message schema
│       ├── routes/
│       │   ├── auth.route.js           # Auth endpoints
│       │   └── message.route.js        # Message endpoints
│       ├── seeds/
│       │   └── user.seed.js            # Database seeder
│       └── index.js                    # Entry point
│
└── frontend/
    └── src/
        ├── components/
        │   ├── AuthImagePattern.jsx     # Decorative auth page pattern
        │   ├── ChatContainer.jsx        # Main chat window
        │   ├── ChatHeader.jsx           # Chat header with user info
        │   ├── MessageInput.jsx         # Message & image input bar
        │   ├── Navbar.jsx               # Top navigation bar
        │   ├── NoChatSelected.jsx       # Empty state for chat
        │   ├── Sidebar.jsx              # Contacts sidebar
        │   └── skeleton/
        │       ├── MessageSkeleton.jsx  # Loading skeleton for messages
        │       └── SidebarSkeleton.jsx  # Loading skeleton for sidebar
        ├── constants/
        │   └── index.js                 # Theme list constants
        ├── lib/
        │   ├── axios.js                 # Axios instance
        │   └── utils.js                 # Helper functions (e.g. formatMessageTime)
        ├── pages/
        │   ├── HomePage.jsx             # Main chat layout
        │   ├── LoginPage.jsx            # Login form
        │   ├── ProfilePage.jsx          # Profile view & update
        │   ├── SettingsPage.jsx         # Theme selector
        │   └── SignUpPage.jsx           # Registration form
        ├── store/
        │   ├── useAuthStore.js          # Auth state + socket management
        │   ├── useChatStore.js          # Chat state + real-time messaging
        │   └── useThemeStore.js         # Theme state (persisted to localStorage)
        └── App.jsx                      # Root component with routing
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js v18+
- MongoDB Atlas account (or local MongoDB)
- Cloudinary account

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/syncchat.git
cd syncchat
```

### 2. Set Up Backend

```bash
cd backend
npm install
```

Create a `.env` file in the `backend/` directory:

```env
PORT=5001
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
NODE_ENV=development
```

### 3. Set Up Frontend

```bash
cd ../frontend
npm install
```

### 4. Run the App

**Backend** (from `backend/` directory):
```bash
npm run dev
```

**Frontend** (from `frontend/` directory):
```bash
npm run dev
```

The frontend will be available at `http://localhost:5173` and the backend at `http://localhost:5001`.

---

## 🔒 Security Features

- Passwords hashed with **bcryptjs** (salt rounds: 10)
- JWT tokens stored in **HTTP-only cookies** (prevents XSS)
- `sameSite: "strict"` cookie policy (prevents CSRF)
- Secure cookies enabled in production
- Protected routes via `protectRoute` middleware

---

## 📦 Scripts

### Backend
| Script | Command |
|---|---|
| Development | `npm run dev` |
| Production | `npm start` |

### Frontend
| Script | Command |
|---|---|
| Development | `npm run dev` |
| Build | `npm run build` |
| Preview | `npm run preview` |
| Lint | `npm run lint` |



## 👨‍💻 Author

Built with ❤️ — feel free to reach out or star ⭐ the repo if you found it useful!
