# 🎓 Professor Office Hour Scheduler

A full-stack web application that helps university students easily book office hour appointments with professors in an organized and conflict-free way.

This project is designed to simplify academic communication and replace manual scheduling with a structured digital system.

---

## 🚀 Features

### 👨‍🎓 Student Features
- Register and login securely
- View list of professors
- See available office hour slots
- Book appointment slots
- Cancel bookings
- View booking history

### 👨‍🏫 Professor Features
- Create and manage office hours
- Set available time slots
- View student bookings
- Cancel or manage appointments

### 🔐 System Features
- Role-based authentication (Student / Professor)
- Prevent double booking of slots
- Time conflict validation
- Secure login using JWT

---

## 🛠️ Tech Stack

### Frontend
- React.js
- Tailwind CSS
- Axios

### Backend
- Node.js
- Express.js
- MongoDB (Mongoose)

### Authentication
- JSON Web Token (JWT)
- bcrypt.js for password hashing

---



## 🧱 Project Structure

```bash
project-root/
│
├── client/                 # Frontend (React)
│   ├── src/
│   ├── components/
│   ├── pages/
│   ├── assets/
│   ├── App.js
│   └── index.js
│
├── server/                 # Backend (Node.js + Express)
│   ├── models/
│   ├── routes/
│   ├── controllers/
│   ├── middleware/
│   ├── config/
│   └── server.js
│
├── .env
├── package.json
└── README.md
```

## 🧠 Database Models

### User
- name
- email
- password
- role (student | professor)

### Professor Profile
- userId
- department
- officeHours (day, startTime, endTime)

### Booking
- studentId
- professorId
- date
- startTime
- endTime
- status (booked | cancelled | completed)

---

## 🔌 API Endpoints

### Auth
- `POST /api/auth/register`
- `POST /api/auth/login`

### Professor
- `POST /api/professor/office-hours`
- `GET /api/professor/bookings`

### Student
- `GET /api/professors`
- `GET /api/professor/:id/slots`
- `POST /api/bookings`
- `DELETE /api/bookings/:id`

---

## ⚙️ How It Works

1. Professors set their available office hours
2. System generates available time slots
3. Students browse professors and book slots
4. System prevents overlapping bookings
5. Both parties can manage appointments from dashboard

---

