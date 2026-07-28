# 🚀 ApexPulse Operations Dashboard

## 📖 Overview

**ApexPulse** is a modern full-stack operations dashboard designed to monitor server infrastructure, display key performance indicators (KPIs), and provide system log insights through an intuitive web interface.

The project combines a **FastAPI** backend with a **Vue 3** frontend to demonstrate the integration of RESTful APIs with a responsive single-page application. ApexPulse provides users with real-time operational data in a clean and interactive dashboard.

---

# 🛠️ Technologies Used

### Frontend

* ⚡ Vue 3
* 🎨 CSS3
* 🌐 Axios
* ⚡ Vite

### Backend

* 🐍 Python
* 🚀 FastAPI
* 🔄 Uvicorn
* 📦 JSON (Data Source)

### Deployment

* ☁️ Render (Frontend)
* ☁️ Render (Backend)
* 🗂️ GitHub

---

# 📂 Project Structure

```text
ApexPulseCopy
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── Backend/
│   ├── app.py
│   ├── data/
│   ├── requirements.txt
│   └── ...
│
└── README.md
```

---

# ⚙️ Installation & Setup

## 1️⃣ Clone the Repository

```bash
git clone <repository-url>
cd ApexPulseCopy
```

---

## 2️⃣ Backend Setup

Navigate to the backend folder:

```bash
cd Backend
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Start the FastAPI server:

```bash
uvicorn app:app --reload
```

The backend will run at:

```text
http://127.0.0.1:8000
```

Swagger API documentation:

```text
http://127.0.0.1:8000/docs
```

---

## 3️⃣ Frontend Setup

Navigate to the frontend folder:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Run the development server:

```bash
npm run dev
```

The frontend will run at:

```text
http://localhost:5173
```

---

# 🌍 Production Deployment

### Frontend

```
https://apexpulse-frontend.onrender.com
```

### Backend API

```
https://apexpulse-backend-api.onrender.com
```

---

# 🔌 API Documentation

## Base URL

```
https://apexpulse-backend-api.onrender.com
```

### Available Endpoints

### 🏠 Home

```
GET /
```

Returns a welcome message.

---

### 📊 Dashboard Summary

```
GET /api/summary
```

Returns dashboard KPI statistics.

---

### 🖥️ Server Fleet

```
GET /api/servers
```

Returns all monitored servers.

Optional query parameter:

```
GET /api/servers?status=Online
```

---

### 📜 System Logs

```
GET /api/logs
```

Returns all system logs.

Optional query parameter:

```
GET /api/logs?level=Error
```

---

# ✨ Features

* 📈 Dashboard KPI cards
* 🖥️ Server monitoring
* 📜 System log viewer
* 🔍 Dynamic API filtering
* 🔄 Live API integration
* 📱 Responsive user interface
* ⚡ FastAPI REST API
* 🌐 Axios-powered frontend communication

---

# 👥 Team Reflection

### 🐍 Python API Construction vs Vue 3 Frontend Logic

Our team divided responsibilities by separating the backend and frontend into independent development tasks. The backend focused on building the FastAPI REST API, creating endpoints, loading dashboard data from JSON files, and ensuring the API returned structured responses. The frontend concentrated on developing the Vue 3 user interface, displaying dashboard metrics, retrieving data with Axios, and presenting information in a responsive and user-friendly layout. This separation allowed both sides to progress simultaneously while integrating through clearly defined API endpoints.

---

### 🌐 Technical Challenges

One of the biggest technical challenges was configuring Cross-Origin Resource Sharing (CORS). During deployment, the frontend initially received browser CORS errors because only the local development URL had been permitted. Updating the FastAPI CORS configuration to include the deployed frontend URL resolved the issue and allowed successful communication between both services.

Another challenge involved dynamically binding Vue components to API data. Since dashboard values were loaded asynchronously, components needed to handle loading states correctly and update dynamically when API responses became available. Proper reactive data handling and Axios integration ensured the interface remained responsive and displayed live information correctly.

---

### 🌱 Git Branching & Pull Requests

Using Git branches allowed different features to be developed independently without affecting the stable version of the project. Pull Requests provided an opportunity to review changes before merging them into the main branch, helping to identify potential issues early and reducing merge conflicts. This workflow made collaboration more organised and ensured that code integration remained smooth throughout development.

---

### 🚀 Future Improvements

If given another sprint cycle, our highest priority would be replacing the JSON data source with a fully integrated SQL database. This would allow real-time data persistence, improve scalability, and better simulate a production-ready operations dashboard. Additional enhancements could include user authentication, role-based access control, live dashboard updates using WebSockets, and advanced analytics for server monitoring.

---

# 🙌 Acknowledgements

Thank you to everyone who contributed to the development of ApexPulse. This project provided valuable experience in full-stack web development, API integration, deployment, collaborative Git workflows, and modern frontend development using Vue 3 and FastAPI.

---

⭐ Thank you for viewing the ApexPulse Operations Dashboard!
