# Smart Campus Management Platform | DevFusion 4.0 Hackathon Solution

A production-ready, full-stack centralized EdTech SaaS platform where **Students**, **Faculty**, **Coordinators**, and **Administrators** interact seamlessly through role-authenticated portals.

---

## 🏆 Hackathon Features & Module Overview

### 1. **Authentication & RBAC Security Engine**
* **Google OAuth 2.0 & Email/Password Authentication** with `bcryptjs` password hashing.
* **Role-Based Access Control (RBAC)**: Route protection middleware enforcing strict segmentation across `/api/student/*`, `/api/faculty/*`, `/api/coordinator/*`, and `/api/admin/*`.
* **Input Validation**: `Zod` schema parsing for all incoming API payloads.

### 2. **UI/UX & Design System (Tailwind CSS)**
* **Dark / Light Mode**: Integrated `next-themes` provider with instant theme switcher.
* **Glassmorphism Component Library**: Translucent frosted glass containers, dynamic stats widgets, shimmer loading skeletons, collapsible navigation sidebar, and searchable data tables with pagination.

### 3. **Role-Based Portals**
* **Student Dashboard**: Class schedules, attendance percentage gauge (`94.5%`), pending assignment submission queue, placement drive alerts, and campus notices.
* **Faculty Dashboard**: Quick action triggers (*Create Assignment*, *Take Attendance*, *Upload Study Material*, *Post Notice*), submission review queue with grading modal.
* **Coordinator Dashboard**: Event management center, live seat availability counters, and event check-in scanner.
* **Admin Dashboard**: System health overview (`99.98%` uptime), user management & role reassignment, security audit action logs, and Recharts analytics.

### 4. **Core Feature Modules**
* **Attendance**: Faculty session QR generator (5-min expiration) & student camera QR scanner simulation.
* **Assignments**: PDF/ZIP file drag-and-drop or GitHub repository submission URLs; rubrics grading & feedback inspector.
* **Events**: Automated digital ticket pass generation (`TCK-XXXXXX`) with downloadable PDF passes.
* **Placements**: 1-click apply with stored resume & interactive application status timeline tracker (`Applied` ➔ `Shortlisted` ➔ `Interviewing` ➔ `Selected`).
* **Real-time Notifications**: Bell popover with unread badge indicators and categorized alerts.

### 5. **Hackathon Bonus Booster Features**
* 🤖 **Gemini AI Campus FAQ Chatbot**: Floating AI assistant answering student queries regarding campus policies, minimum attendance rules (75%), and placement criteria.
* 📊 **Recharts Analytics & CSV Exporter**: AreaCharts, BarCharts, and Donut PieCharts for monthly attendance, department performance, CTC brackets, plus 1-click CSV/Excel report downloads.
* 🐳 **Dockerized Deployment**: Includes `Dockerfile` for frontend, `Dockerfile` for backend, and a unified `docker-compose.yml`.
* 📄 **OpenAPI / Swagger Documentation**: Interactive API spec viewer at `/api-docs`.

---

## 🔑 Test Credentials for Hackathon Judges

| Role | Email | Password | Pre-configured Access |
| :--- | :--- | :--- | :--- |
| **Student** | `student@campus.edu` | `student123` | Access Student Dashboard, Attendance %, Assignments, QR Pass, Job Apply |
| **Faculty** | `faculty@campus.edu` | `faculty123` | Access Faculty Dashboard, Create Assignment, QR Session, Grading Queue |
| **Coordinator** | `coordinator@campus.edu` | `coord123` | Access Coordinator Dashboard, Event Manager, Ticket Check-in |
| **Admin** | `admin@campus.edu` | `admin123` | Access Admin Dashboard, User Role Editor, Audit Logs, CSV Exporters |

---

## 💻 Local Setup & Installation

### Option 1: Standard Node.js Execution

```powershell
# 1. Clone or navigate to the repository
cd hackathon

# 2. Run Backend
cd smart-campus-backend
npm install
npm run dev

# 3. Run Frontend (in a second terminal)
cd ../smart-campus-frontend
npm install
npm run dev
```

* **Frontend URL**: `http://localhost:3000`
* **Backend API Health**: `http://localhost:5000/api/health`

### Option 2: 1-Command Docker Compose

```powershell
docker-compose up -d
```

---

## 🌐 Production Deployment Guide

* **Frontend**: Deploy `smart-campus-frontend` to **Vercel** (`npx vercel`).
* **Backend**: Deploy `smart-campus-backend` to **Render** / **Railway** with `MONGODB_URI` environment variable pointing to MongoDB Atlas.
