# ⚡ HackFest 1.0 — AWS SBG MNNIT Allahabad

[![Vite](https://img.shields.io/badge/Frontend-Vite%20%2B%20React-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![TailwindCSS](https://img.shields.io/badge/Styling-TailwindCSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Node.js](https://img.shields.io/badge/Backend-Node.js%20%2B%20Express-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB%20Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![Render](https://img.shields.io/badge/Hosted-Render.com-46E3B7?style=for-the-badge&logo=render&logoColor=white)](https://render.com/)

An enchanted, Harry Potter-themed full-stack hackathon web application built for **HackFest 1.0**, presented by the **AWS Student Builder Group (AWS SBG)** at **MNNIT Allahabad**.

---

## ✨ Features

- 🧙‍♂️ **Hogwarts Sorting Ceremony**: Interactive Sorting Hat mechanism assigning builders into Gryffindor, Slytherin, Ravenclaw, or Hufflepuff.
- ⚡ **The Triwizard Challenge**: 72-hour online hackathon sprint tracking system for shortlisted teams.
- 🏰 **The Hogwarts Championship**: Offline Grand Finale stage management with live real-time updates.
- 🤝 **Teammate & Team Management**: Create teams, invite members, send join requests, and search available teammates with live Socket.io notifications.
- 🎁 **Prizes & Rewards Section**: ₹1,00,000+ Prize Pool display, official certificates, swag kits, and AWS Cloud credits.
- 🎫 **QR Pass & Event Check-in**: Dynamic QR code pass generation for registered participants with live venue check-in scanner for organizers.
- 👑 **Super Admin Dashboard**: Full admin panel to manage participants, teams, house distributions, and send broadcast announcements.
- 📜 **Daily Prophet & FAQ**: Dynamic announcements channel and Harry Potter-styled interactive accordion FAQ section.
- 🌌 **Cinematic Parallax UI**: Glassmorphic dark aesthetic, 3D card tilt effects, particle sparks, and smooth Framer Motion layered transitions.

---

## 🛠️ Tech Stack

### **Frontend**
- **Framework**: React 18 (Vite)
- **Styling**: Vanilla CSS, TailwindCSS, Custom Hogwarts Design System
- **Animations**: Framer Motion (Parallax depth & 3D card tilt)
- **Routing**: React Router DOM v6
- **Real-Time**: Socket.io-client
- **HTTP Client**: Axios with centralized interceptors
- **Icons & Alerts**: Lucide React, React Hot Toast

### **Backend**
- **Runtime**: Node.js (ES Modules)
- **Framework**: Express.js (v5)
- **Database**: MongoDB Atlas via Mongoose ODM
- **Authentication**: JWT (JSON Web Tokens) & BcryptJS password hashing
- **Real-Time**: Socket.io server with room-based user notifications
- **Utilities**: QRCode generator, Cors, Dotenv

---

## 📁 Repository Structure

```
AWS-WEB/
├── backend/
│   ├── src/
│   │   ├── config/          # Database configuration (db.js)
│   │   ├── controllers/     # Auth, User, Team, Admin controllers
│   │   ├── middleware/      # JWT Auth & SuperAdmin authorization
│   │   ├── models/          # MongoDB schemas (User, Team, Notification, etc.)
│   │   └── routes/          # Express API route endpoints
│   ├── app.js               # Express application initialization
│   ├── index.js             # HTTP server & Socket.io entry point
│   ├── package.json
│   └── .env                 # Environment configuration
├── frontend/
│   ├── public/
│   │   └── images/          # Assets, house crests, backgrounds, posters
│   ├── src/
│   │   ├── components/      # Navbar, Hero, AboutEvent, RewardsSection, etc.
│   │   ├── pages/           # Dashboard, Login, Signup, FindTeam, QRPass, Admin
│   │   ├── services/        # Axios API client setup
│   │   ├── App.jsx          # Router & layered section layout
│   │   └── index.css        # Core design system & Hogwarts typography
│   ├── package.json
│   └── vite.config.js
└── render.yaml              # Render.com deployment blueprint
```

---

## 🚀 Quick Start (Local Development)

### **Prerequisites**
- Node.js (v18 or higher)
- npm or yarn
- MongoDB Atlas cluster URL

---

### **1. Backend Setup**

```bash
# Navigate to backend folder
cd backend

# Install dependencies
npm install

# Create .env file
```

Create a `.env` file in the `backend/` directory:

```env
PORT=5000
NODE_ENV=development
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
SUPER_ADMIN_EMAILS=malika237581@gmail.com,divine.throne0024@gmail.com
CLIENT_URL=http://localhost:5173
```

Run backend server:
```bash
# Development mode with nodemon
npm run dev
```

The backend server runs on `http://localhost:5000`.

---

### **2. Frontend Setup**

```bash
# Open a new terminal and navigate to frontend folder
cd frontend

# Install dependencies
npm install

# Start Vite dev server
npm run dev
```

The frontend web app runs on `http://localhost:5173`.

---

## 🌐 Deployment Instructions

### **Backend (Render.com)**
1. Connect your GitHub repository to [Render.com](https://render.com).
2. Create a new **Web Service** pointing to the `backend` root directory.
3. Set Environment Variables:
   - `MONGO_URI`: `your_mongodb_connection_string`
   - `JWT_SECRET`: `your_jwt_secret`
   - `CLIENT_URL`: `https://your-frontend.vercel.app`
   - `NODE_ENV`: `production`

---

### **Frontend (Vercel)**
1. Connect your repository to [Vercel](https://vercel.com).
2. Set Framework Preset to **Vite**.
3. Add Environment Variable:
   - `VITE_API_URL`: `https://your-backend-service.onrender.com/api`
4. Deploy!

---

## 👥 Organizers & Credits

Organized with 💛 by the **AWS Student Builder Group (AWS SBG)** at **MNNIT Allahabad**.

- **Lead Organizers**: AWS SBG Core Team
- **Event**: HackFest 1.0 (2026)

---

## 📄 License

This project is licensed under the [ISC License](LICENSE).
