# 🔍 Forensic Management System (Django + DRF)

A secure and efficient web-based system designed to manage crime cases, suspects, evidence, storage locations, and chain-of-custody records.  
Built using **Django** and **Django REST Framework**, this project ensures proper forensic documentation and safe evidence handling as per investigation standards.

---

# 🚀 Features

## 📝 Case Management
- Add and track criminal cases
- Priority levels (Low, Medium, High, Critical)
- Open/Closed status
- Officer responsible for case creation

## 🧑‍💼 User Roles
- Admin  
- Investigator  
- Forensic Officer  
- Evidence Clerk  
- Analyst  

Each user is linked to a role.

## 🧪 Evidence Management
- Add evidence linked to cases
- Multiple evidence types:
  - Digital  
  - Biological  
  - Physical  
  - Document  
- Store evidence condition & status
- Track:
  - Who collected it  
  - Who currently holds it  
  - Where it is stored  
  - Description and metadata  

## 🔗 Chain of Custody Tracking
Each movement of evidence is recorded with:
- From holder → To holder  
- From location → To location  
- Time & Date  
- Performed by  
- Remarks  

This ensures **tamper-proof** forensic tracking.

## 📦 Storage Location Management
- Add forensic lockers, vaults, freezers, and storage rooms
- Assign evidence to locations
- Track where evidence currently is

---

# 🗄️ Database Schema (Important for Viva)

## ⭐ Main Tables
- Role  
- UserAccount  
- CaseInfo  
- Evidence  
- EvidenceType  
- StorageLocation  
- Suspect  
- ChainOfCustodyLog  

## ⭐ Relationships (Text ER Diagram)

```
Role ───< UserAccount
UserAccount ───< CaseInfo
CaseInfo ───< Evidence ───< ChainOfCustodyLog
EvidenceType ───< Evidence
StorageLocation ───< Evidence
```

---

# 🧩 API Endpoints (Django REST Framework)

## 🔹 Cases
```shell
GET    /api/cases/
POST   /api/cases/
PUT    /api/cases/<id>/
DELETE /api/cases/<id>/
```

## 🔹 Evidence
```shell
GET    /api/evidence/
POST   /api/evidence/
PUT    /api/evidence/<id>/
DELETE /api/evidence/<id>/
```

## 🔹 Evidence Transfer (Star Feature)
```shell
POST /api/transfer/
```

## 🔹 Suspects
```shell
GET /api/suspects/
POST /api/suspects/
PUT /api/suspects/<id>/
DELETE /api/suspects/<id>/
```

---

# ⚙️ Running the Project (Setup Instructions)

## 1️⃣ Create Virtual Environment
```shell
python -m venv venv
```

## 2️⃣ Activate Virtual Environment
### On Windows:
```shell
venv\Scripts\activate
```

### On Mac/Linux:
```shell
source venv/bin/activate
```

## 3️⃣ Install Dependencies
```shell
pip install -r requirements.txt
```

## 4️⃣ Apply Migrations
```shell
python manage.py migrate
```

## 5️⃣ Run the Server
```shell
python manage.py runserver
```

### Access URLs:
- **API Root:** http://127.0.0.1:8000/api/  
- **Admin Panel:** http://127.0.0.1:8000/admin/

---

# 🔐 Admin Credentials (for Demo)
```
Username: admin
Password: 123
```

---

# 🗃️ Seed Data
The database includes:
- Roles  
- Users  
- Evidence Types  
- Storage Locations  
- Cases  
- Suspects  
- Evidence  
- ChainOfCustody Logs  

---

# 🎯 Purpose of the Project
This project is developed as part of the **DBMS Laboratory Course**, demonstrating:

- Relational database design  
- Django ORM  
- REST API development  
- Foreign key relationships  
- Evidence chain tracking  
- CRUD operations  
- Normalized multi-table schema  

---

# 👨‍💻 Author
**Niramay Madhav Narayan**  
B.Tech CSE  
Forensic Management System – DBMS Laboratory Project  

---
