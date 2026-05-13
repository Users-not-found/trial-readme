# Nova Monitor 🚀

A 100% local-first API monitoring workspace and uptime tracker. Build, save, and continuously monitor your API endpoints without relying on cloud services.

<hr style="height: 0.5px; opacity: 0.2;">

## ✨ Features
* **Local-First:** All requests and logs are stored locally using SQLite.
* **Continuous Monitoring:** Set custom intervals (e.g., every 1 min) to ping APIs automatically in the background.
* **Live Dashboard:** Real-time latency charts and uptime status.
* **Workspace Engine:** Full support for GET/POST requests.
* **Dark Aesthetic:** Sleek, charcoal dark-mode UI built with Tailwind CSS.

<hr style="height: 1px; opacity: 0.15; width: 90%; margin: auto;">

## 💻 Tech Stack
* **Backend:** Python, FastAPI, SQLAlchemy, APScheduler
* **Frontend:** React, Vite, Tailwind CSS v3, Recharts
* **Database:** SQLite

<hr style="height: 1px; opacity: 0.15; width: 90%; margin: auto;">

## 🛠️ Installation & Setup

### Prerequisites
* Python 3.8+
* Node.js (v18+)

### 1. Backend Setup (FastAPI)
Open a terminal and navigate to the `backend` directory.
```
# Navigate to the backend folder
cd backend

# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# On Windows:
.\venv\Scripts\activate
# On Mac/Linux:
# source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start the server
uvicorn main:app --reload --port 8001

```

The API will be available at *http://127.0.0.1:8001*
Interactive API Docs: *http://127.0.0.1:8001/docs*

### 2. Frontend Setup (React + Vite)
Open a new terminal and navigate to the frontend directory.
```
# Navigate to the frontend folder
cd frontend

# Install Node modules
npm install
npm install -D tailwindcss@3 postcss autoprefixer
npm install axios lucide-react recharts date-fns

# Start the development server
npm run dev
```
The Dashboard will be available at *http://localhost:5173*

<hr style="height: 1px; opacity: 0.15; width: 90%; margin: auto;">

## 🚀 Usage
Ensure both the Backend and Frontend servers are running simultaneously.

Open your browser and go to *http://localhost:5173*

Click New Request to add an API endpoint.

Set the method, URL, and polling interval (in minutes).

Click Save to start live monitoring. Use the Pause/Resume buttons to control the tracker.

## Final Folder Structure
```
nova-monitor/
├── README.md                      
│
├── backend/
│   ├── venv/                      # (Auto-generated Python environment)
│   ├── routers/
│   │   ├── monitor.py             
│   │   └── workspace.py           
│   ├── api_monitor.db             # (Auto-generated SQLite database)
│   ├── database.py                
│   ├── main.py                    
│   ├── models.py                  
│   ├── requirements.txt           
│   └── schemas.py                 
│
└── frontend/
    ├── node_modules/              # (Auto-generated React dependencies)
    ├── public/
    │   └── vite.svg               
    ├── src/
    │   ├── App.jsx                
    │   ├── index.css              
    │   └── main.jsx               
    ├── index.html                 
    ├── package-lock.json          
    ├── package.json               
    ├── postcss.config.js          
    ├── tailwind.config.js         
    └── vite.config.js

```
