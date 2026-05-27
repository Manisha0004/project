# Inventory Stock Tracker & Demand Planner

This project is a coding test that has two main parts:
1. **Backend**: A Python web API built with FastAPI that stores stock entries in a SQLite database and validates all input data.
2. **Frontend**: A React dashboard where users can filter, sort, view detailed summaries, and add new stock entries.

---

## 1. What you need installed
- **Python**: Version 3.9 or higher (Python 3.13 is recommended).
- **Node.js**: Version 18.0 or higher.

---

## 2. Setting up the Backend (API & Database)

### Step 1: Go into the backend folder
Open your terminal and type:
```powershell
cd backend
```

### Step 2: Set up a Python virtual environment
Create a virtual environment (we specify the Python 3.13 path here since the default on this machine is older):
```powershell
& "C:\Program Files\Python313\python.exe" -m venv venv
```
Activate it:
```powershell
.\venv\Scripts\Activate.ps1
```

### Step 3: Install all packages
```powershell
pip install -r requirements.txt
```

### Step 4: Add the initial data to your database
We configured the database to use your file at `D:\Downloads\database\manishadb`.
To load the initial 80 entries from the frontend's dataset, run:
```powershell
python seed_db.py
```

### Step 5: Start the backend server
```powershell
uvicorn app.main:app --reload
```
You should see a message in the terminal showing `SQLite Database connected successfully!`.
You can view the interactive API docs at:
**[http://localhost:8000/docs](http://localhost:8000/docs)**

### Step 6: Run the automated tests (optional)
To make sure everything is working as expected, run:
```powershell
pytest -v
```

---

## 3. Setting up the Frontend (React App)

### Step 1: Open a new terminal tab and go to the frontend folder
```powershell
cd frontend
```

### Step 2: Install dependencies
```powershell
npm install
```

### Step 3: Start the frontend development server
```powershell
npm run dev
```
Open your browser and visit:
**[http://localhost:5173/](http://localhost:5173/)**
