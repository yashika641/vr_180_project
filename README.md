 
# VR180 Backend 🚀

A **FastAPI + Supabase** backend for the **VR180 project**, providing APIs for user management and authentication.  
This backend connects to **Supabase (PostgreSQL + Auth)** for database operations and exposes a RESTful API for the frontend or mobile app.  

---

## 📂 Project Structure
```

backend/
│── app/
│   ├── db.py                 # Supabase client setup
│   ├── main.py               # FastAPI entrypoint
│   ├── models/
│   │   └── user_model.py     # Pydantic models for users
│   ├── routes/
│   │   └── user_routes.py    # CRUD routes for users
│   └── **init**.py
│
│── .env                      # Environment variables (Supabase keys)
│── requirements.txt          # Python dependencies
│── README.md                 # Project documentation

````

---

## ⚡ Features
- 📦 Supabase (PostgreSQL) integration  
- 🔑 Secure user model with UUIDs  
- ✨ CRUD operations for users (`create`, `read`, `update`, `delete`)  
- 🛠 RESTful API with FastAPI  
- 📑 Auto-generated API docs at `/docs`  

---

## 🛠 Setup Instructions

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/vr180-backend.git
cd vr180-backend
````

### 2️⃣ Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Configure environment variables

Create a `.env` file in the root:

```
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_KEY=your-service-role-key
```

### 5️⃣ Run the server

```bash
uvicorn app.main:app --reload
```

---

## 📡 API Endpoints

| Method | Endpoint      | Description         |
| ------ | ------------- | ------------------- |
| POST   | `/users/`     | Create a new user   |
| GET    | `/users/`     | Get all users       |
| GET    | `/users/{id}` | Get user by ID      |
| PUT    | `/users/{id}` | Update user details |
| DELETE | `/users/{id}` | Delete user         |

👉 Interactive Swagger Docs: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 📦 Dependencies

* [FastAPI](https://fastapi.tiangolo.com/) – web framework
* [Uvicorn](https://www.uvicorn.org/) – ASGI server
* [Supabase-py](https://github.com/supabase-community/supabase-py) – Supabase client for Python
* [Pydantic](https://docs.pydantic.dev/) – data validation
* [python-dotenv](https://pypi.org/project/python-dotenv/) – load environment variables

---

## 🚀 Deployment

You can deploy on:

* [Render](https://render.com/)
* [Railway](https://railway.app/)
* [Vercel + Supabase](https://vercel.com/)
* [Docker](https://www.docker.com/) (optional)

---

## 📌 Notes

* Supabase provides **`auth.users`** table automatically.
* We created a custom `profiles` table for extra user info (username, avatar, etc.).
* Authentication logic (JWT, login, register) can be added later.

---

## 👩‍💻 Author

**VR180 Team**
📧 Contact: [your-email@example.com](mailto:palyashika641@gmail.com)

