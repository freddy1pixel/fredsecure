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



## 🔧 Installation

### 1. Clone the repo
```bash
git clone https://github.com/your-username/fred-secure-meetings.git
cd fred-secure-meetings



---

## 🧩 Project Structure

fred-secure-meetings/
├── backend/              # Express backend + SQLite
├── frontend/             # React + Tailwind + Vite
├── database/fredsecure.db  # SQLite file (auto-created if missing)
└── README.md

## Front End Setup




