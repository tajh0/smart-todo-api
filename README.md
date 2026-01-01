# 📝 Smart ToDo API

Smart ToDo API is a RESTful backend application built using **FastAPI** and **MongoDB**.  
It provides secure **JWT-based authentication** and allows users to manage their tasks with full **CRUD operations**.

---

## 🚀 Features

- User Registration & Login  
- JWT Authentication (Bearer Token)  
- Create, Read, Update, Delete (CRUD) Tasks  
- MongoDB Database Integration  
- Interactive Swagger Documentation  
- Secure Password Hashing (bcrypt)  

---

## 🛠 Technology Stack

- **Backend:** FastAPI (Python)  
- **Database:** MongoDB  
- **Authentication:** JWT (OAuth2PasswordBearer)  
- **Security:** passlib + bcrypt  
- **Documentation:** Swagger (OpenAPI)  

---

## 📂 Project Structure

```
smart-todo-api/
│
├── app/
│   ├── main.py
│   ├── auth.py
│   ├── database.py
│   ├── models.py
│   └── utils.py
│
├── .env.example
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Create Virtual Environment
```bash
python -m venv venv
venv\Scripts\activate
```

### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 🗄 MongoDB Setup

- Install MongoDB Community Server  
- Ensure MongoDB service is running on port `27017`  

```powershell
net start MongoDB
```

---

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
MONGO_URI=mongodb://localhost:27017
MONGO_DB=smart_todo_db
SECRET_KEY=your_secret_key_here
ACCESS_TOKEN_EXPIRE_MINUTES=60
```

---

## ▶️ Run the Application

```bash
uvicorn app.main:app --reload
```

Application will be available at:
```
http://127.0.0.1:8000
```

---

## 📘 Swagger Documentation

Open in browser:
```
http://127.0.0.1:8000/docs
```

---

## 🔑 API Usage Flow

1. Register → `/auth/register`  
2. Login → `/auth/login`  
3. Copy access token  
4. Authorize using Bearer token  
5. Manage tasks using `/tasks`  

---

## 🔒 Authorization Header

```
Username
Password
or
Authorization: Bearer <access_token>
```

---

## 📌 Example Register Request

```json
{
  "email": "user@gmail.com",
  "password": "123456"
}
```

---

## 📌 Example Login Request (Form Data)

```
username=user@gmail.com
password=123456
```

---

## ⚠️ Common Errors

- **401 Unauthorized:** Token missing or expired  
- **500 Server Error:** MongoDB not running or dependency issue    

---

## 👨‍💻 Author

Naimul Hossain
