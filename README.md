# Fred Secure Meetings

Fred Secure Meetings is a modern, secure, and Google Meet–styled video conferencing platform that supports user accounts, call scheduling, profile management, and Jitsi-powered video calls. Built with React (frontend), Express + SQLite (backend), and custom Jitsi integration.

---

## 🚀 Features

- 🔐 **Multi-user authentication** using JWT
- 🗓️ **Schedule meetings** with title, date, and time
- 📋 **Dashboard** showing upcoming meetings, past calls, and usage stats
- 📜 **Transcripts** of past meetings viewable by participants
- 🎥 **Live video rooms** using Jitsi (self-hosted or meet.jit.si)
- 👤 **Edit profile** with image and name updates
- 🧠 **Smart UI**: disables buttons when forms are incomplete
- 🔔 **Error handling** and toast feedback for actions

---

## 🧱 Tech Stack

| Layer       | Tech                                    |
|-------------|-----------------------------------------|
| Frontend    | React + Tailwind CSS + React Router     |
| Backend     | Node.js + Express + SQLite (via knex)   |
| Auth        | JWT (stored in `localStorage`)          |
| Video Calls | Jitsi Meet (embedded in React)          |

---

## 🧩 Project Structure

```
fred-secure-meetings/
├── backend/              # Express backend
│   ├── routes/           # Auth, user, meeting APIs
│   └── db/               # SQLite setup
├── frontend/             # React app with Tailwind
│   ├── pages/            # Login, Register, Dashboard, VideoRoom, etc.
│   └── components/       # Navbar, ProfileModal, etc.
├── database/
│   └── fredsecure.db     # SQLite database file
├── public/               # Logo, favicon, assets
└── README.md
```

---

## ⚙️ Installation Guide

### Prerequisites

- Node.js ≥ 18.x
- npm
- SQLite (preinstalled)
- (Optional) Your own Jitsi server

---

### 🖥 Backend Setup

```bash
cd backend
npm install
node app.js
```

> Runs on: `http://localhost:5000`  
> DB: `fredsecure.db` auto-generated if missing

---

### 💻 Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

> Vite dev server: `http://localhost:5173`  
> Communicates with backend via relative `/api` routes

---

## 📡 API Summary

### Auth

- `POST /api/register` — `{ name, email, password }`
- `POST /api/login` — `{ email, password }`

### Meetings

- `POST /api/meetings/schedule` — `{ title, datetime, duration }`
- `GET /api/meetings/upcoming`
- `GET /api/meetings/past`
- `GET /api/meetings/stats`

### User

- `POST /api/users/update-profile` — `{ name, avatarUrl }`

---

## 🛠 Deployment Tips

- Point your custom domain (e.g., `meet.fredsecure.xyz`) to a VPS
- Install and run a Jitsi Docker stack or `apt`-based Jitsi instance
- Update the frontend's `VideoRoom.jsx` to use your domain:
  ```js
  const domain = "meet.fredsecure.xyz";
  ```

---

## 🖼️ Screenshots (Optional)

| Dashboard | Meeting | Edit Profile |
|-----------|---------|--------------|
| ![dashboard](screenshots/dashboard.png) | ![meeting](screenshots/meeting.png) | ![profile](screenshots/profile.png) |

---

## 🧠 Notes

- Buttons like **Create/Join** are disabled until title is filled
- Profile modal allows image/name change and persists to DB
- Past meetings show "Transcript" instead of rejoin options
- Forgot Password is handled via email (pending setup)

---

## 🧑‍💻 Author

Built by Fred Acheampong • Inspired by Google Meet

---

## 🪪 License

MIT — free to use, modify, and deploy
