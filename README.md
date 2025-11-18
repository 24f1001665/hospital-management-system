# Hospital Management System

A web application that streamlines hospital operations by managing patients, doctors, appointments, and related records digitally. It improves efficiency and reduces manual work for administrators, doctors, and patients.

---

## 🧱 Features

### **User Roles**
- Admin  
- Doctor  
- Patient  

### **Admin Features**
- Manage users, doctors, patients
- Manage appointments
- View all departments and system data

### **Doctor Features**
- View upcoming appointments
- View patient history

### **Patient Features**
- Browse & search doctors by name or department
- Book appointments

### **Backend Features**
- Database models for:
  - Users  
  - Departments  
  - Appointments  
  - Treatments  
  - DoctorAvailability  
- Secure password hashing (using `werkzeug.security`)
- Timestamps stored in **UTC** for consistency

---

## 🛠 Technology Stack

- Python 3.x  
- Flask (Web Framework)  
- Flask-SQLAlchemy (ORM)  
- SQL Database (SQLite / PostgreSQL)  
- HTML templates (Jinja2)  
- Werkzeug (password hashing)

---

## 📁 Project Structure

```plaintext
hospital-management-system/
│
├── instance/                 # Config files, environment variables
├── templates/                # HTML template files
├── app.py                    # Main Flask application
├── models.py                 # ORM models
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation

```
## 🔧 Getting Started

### **Prerequisites**
- Python 3.x installed  
- Virtual environment recommended  

---

## 🏗 Installation

### **1. Clone the repository**
```bash
git clone https://github.com/24f1001665/hospital-management-system.git
cd hospital-management-system
```

2. Create and activate a virtual environment

Linux / Mac:
```bash
python3 -m venv venv
source venv/bin/activate
```
Windows:
```bash
venv\Scripts\activate
```
3. Install dependencies
```bash
pip install -r requirements.txt
```
4. Initialize the database
```bash 
python app.py
```
The init_db() function inside the project will create all required tables.

5. Start the Flask server
```bash 
python app.py
```
Now open your browser:
👉 http://localhost:5000

### **✅ Usage / Workflow**

- Admin → Manages departments, doctors, patients, appointments

- Patient → Browses doctors → Books appointment

- Doctor → Views upcoming appointments → Opens patient history

### **🛡 Security & Best Practices**

- Password hashing using generate_password_hash

- Use datetime.utcnow() for timestamps

- Role-based authorization with decorators

- For production:

  - Set FLASK_DEBUG=False

  - Use Gunicorn, Nginx, etc.

  - Store secret keys + DB URLs in environment variables










