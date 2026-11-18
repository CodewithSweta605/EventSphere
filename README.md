# 🎟️ EventSphere — Modern Full-Stack Event Booking Platform

<p align="center">
  <strong>A comprehensive MERN stack platform for discovering, organizing, and booking events with two-factor email OTP verification and real-time administrative management.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-18-blue?style=for-the-badge&logo=react" alt="React" />
  <img src="https://img.shields.io/badge/Node.js-Express-green?style=for-the-badge&logo=node.js" alt="Node.js" />
  <img src="https://img.shields.io/badge/MongoDB-Mongoose-brightgreen?style=for-the-badge&logo=mongodb" alt="MongoDB" />
  <img src="https://img.shields.io/badge/TailwindCSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="License" />
</p>

---

## 🌟 Overview

**EventSphere** is an end-to-end web application engineered to streamline event discovery, ticket reservation, and administrative control. It eliminates third-party ticketing friction with native booking management, automated confirmation notifications, and email-based two-factor OTP verification for both authentication and checkout.

---

## 🚀 Key Features

### 🔐 Authentication & Security
- **JWT & Bcrypt Encryption**: Robust session handling and hashed password storage.
- **2FA Email OTP Verification**:
  - Mandatory one-time password sent via Nodemailer to verify account activation.
  - One-time password verification required to validate and authorize ticket reservations.
- **Role-Based Access Control (RBAC)**: Distinct permissions for standard users versus platform administrators.

### 👥 User Capabilities
- **Event Discovery**: Filter and search through upcoming live events, tech conferences, concerts, and workshops.
- **Booking Management**: Submit reservation requests, monitor status in a personalized dashboard, and cancel bookings when necessary.
- **Instant Email Confirmation**: Receive automated confirmation receipts with event details.

### 🛡️ Administrative Dashboard
- **Event Lifecycle Control**: Create, update, or remove free and paid events with custom seat capacity, pricing, categories, and cover images.
- **Booking Approval Workflow**: Review incoming reservations in a live queue, mark payments, and approve or reject ticket requests.
- **Real-Time Analytics**: Monitor metrics including total revenue, confirmed attendees, and pending requests.

---

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| **Frontend** | React 18, Vite, React Router v6, Tailwind CSS, React Icons, Axios |
| **Backend** | Node.js, Express.js, Mongoose, JWT (JSON Web Tokens), Nodemailer |
| **Database** | MongoDB / MongoDB Atlas |
| **Tools & Utilities** | Concurrently, Nodemon, Postman |

---

## 📁 Project Architecture

```
EventSphere/
├── client/                     # Frontend Application (React + Vite + Tailwind)
│   ├── public/                 # Static assets
│   ├── src/
│   │   ├── components/         # Reusable UI components (Navbar, Modals, Cards)
│   │   ├── context/            # React AuthContext & Global state
│   │   ├── pages/              # Views (Home, Login, Register, Admin, Dashboard)
│   │   ├── App.jsx             # Route definitions
│   │   └── main.jsx            # Entry point
│   ├── package.json
│   └── vite.config.js
├── server/                     # Backend Application (Node.js + Express)
│   ├── models/                 # Mongoose schemas (User, Event, Booking)
│   ├── routes/                 # Express API routes (auth, events, bookings)
│   ├── middleware/             # Auth and role verification guards
│   ├── utils/                  # Nodemailer & OTP helper functions
│   ├── seed.js                 # Database seeder script
│   ├── server.js               # Express application entry point
│   └── package.json
├── EventSphere_Postman_Collection.json   # Ready-to-import API test suite
├── package.json                # Root package for unified scripts
└── README.md
```

---

## ⚡ Quick Start

### 1. Prerequisites
- [Node.js](https://nodejs.org/) (v16 or higher)
- [MongoDB](https://www.mongodb.com/) (Local instance or MongoDB Atlas cluster)

### 2. Environment Configuration
Create a `.env` file inside the `server/` directory:

```env
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/eventsphere?retryWrites=true&w=majority
JWT_SECRET=your_jwt_secret_key_here
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_google_app_password
```

> **Note**: For Gmail, generate an **App Password** from your Google Account Security settings (Standard passwords will not work with 2FA enabled).

### 3. Installation & Running (Single Terminal)

From the project root:

```bash
# Install root, backend, and frontend dependencies
npm run install:all

# Launch both backend and frontend concurrently
npm run dev
```

- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:5000

---

## 📬 Postman API Collection

A complete Postman collection is included: `EventSphere_Postman_Collection.json`.
1. Open **Postman** and click **Import**.
2. Select `EventSphere_Postman_Collection.json`.
3. Test end-to-end user journeys (Register $\rightarrow$ OTP Verification $\rightarrow$ Login $\rightarrow$ Create Event $\rightarrow$ Book Ticket $\rightarrow$ Admin Approval).

---

## 👤 Author

**Sweta Kumari**  
- GitHub: [@CodewithSweta605](https://github.com/CodewithSweta605)

---

## 📄 License

This project is licensed under the MIT License.
