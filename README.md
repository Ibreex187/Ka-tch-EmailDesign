# Ka-tch Email Service Front End Case Study

## Overview
This project is a simple email service case study, featuring a Flask backend and a minimal HTML/JS frontend. It supports user registration, login, logout, sending emails, and viewing a dummy inbox. The backend enforces password rules, auto-generates user emails, and clearly labels sent/received emails. All code is well-commented. It is your job to redesign the front-end to serve those services. You are more than welcome to add/propose new features as needed. We are looking for creativity with logically reasoning. 

**WE STRONGLY DO NOT RECOMMEND FOLLOW THE SAME DESIGN AS EXISTING DESIGN SUCH AS GMAIL, OUTLOOK, ETC.** 

You can get bonus points if you modify any part of the back end code, but it is not required in order to pass the case study. For some areas such as connecting the CORS for front-end and back-end part, develop a new api call in the backend, code optimization, or/and etc.

Please read this readme file carefully to understand how to set up & understand the current features that exist inside the backend code.

---

## Features
- User registration with password rules (uppercase, lowercase, number, special symbol, confirmation)
- Auto-generated user email addresses (`<username>@ka-tch.com`)
- Registration fields: first name, last name, date of birth
- User login/logout
- Send email (Flask-Mail integration, demo mode)
- View dummy inbox (with edge-case data, labels for sent/inbox)
- Simple HTML/JS frontend for all features
- Session-based authentication

---

## Prerequisites
- Python 3.10+
- pip (Python package manager)

---

## Setup Instructions

### 1. Clone the Repository
```
git clone https://github.com/Ka-Technology/front-end-case-study-1.git
cd front-end-case-study-1
```

### 2. Set up virtual environment
#### Linux
```
cd backend

python3 -m venv venv

source venv/bin/activate

pip install -r requirements.txt
```

#### Mac OS
```
cd backend

python3 -m venv venv

source venv/bin/activate

pip install -r requirements.txt
```
### Windows
```
cd backend

python -m venv venv

venv\Scripts\activate

pip install -r requirements.txt

```

### 3. Install Python Dependencies
```
cd backend
pip install -r requirements.txt
```

### 4. Run the Flask Backend
```
cd backend
python app.py
```
- The backend will start on `http://127.0.0.1:8080/` by default.


### 5. Run the Frontend (Optional: Using a Simple HTTP Server)
You can serve the frontend using a simple HTTP server so that it runs on a different port than the backend. This is recommended for local development.

#### Using Python (from the project root or `frontend/` folder):
```
cd frontend
python -m http.server 3000
```
- This will serve the frontend at `http://localhost:3000/`.
- Open your browser and go to `http://localhost:3000/` to use the app.

#### Alternative: Using Node.js (if installed)
```
npm install -g serve
cd frontend
serve -l 3000
```

- The frontend will interact with the backend via HTTP requests.
- **It is your job to design, develop, and connect the backend code for it!**

---

## File Structure
```
backend/
  app.py                # Main Flask app
  requirements.txt      # Python dependencies
  routes/
    auth_routes.py      # Auth endpoints (register, login, logout, status)
    mail_routes.py      # Mail endpoints (send, inbox, status)
frontend/
  index.html            # Simple HTML/JS frontend
```

---

## Notes
- All backend endpoints are documented with comments in the code.
- The dummy inbox is in-memory and resets on server restart.
- Password rules are enforced on registration.
- Email sending is simulated for demo/testing.
- The project is for interview purpose.

---

## Author
Ka Technology

---

## License
See `LICENSE` file.