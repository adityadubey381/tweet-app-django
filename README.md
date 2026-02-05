# Tweet App (Django)

A Django-based Tweet application with user authentication.  
Only authenticated users can create and add tweets, while unauthenticated users are restricted.

This project focuses on understanding Django authentication, authorization, routing, and app structure.

---

## Tech Stack

- Python
- Django
- SQLite (development database)
- HTML (Django Templates)
- Git & GitHub

---

## Project Structure

```

tweet-app-django/
├── tweet/                 # Django project (settings, urls)
├── tweets/                # Tweet app
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── templates/
├── manage.py
├── db.sqlite3
├── .gitignore
└── README.md

````

---

## Features

- User authentication (Login / Logout)
- Authentication-based access control
- Only logged-in users can:
  - Create tweets
  - Add new content
- Django built-in auth system
- URL routing using `include()`
- Secure views using login protection

---

## Authentication Logic

- Django’s built-in `auth` system is used
- Protected views use:
  - `@login_required` decorator  
  **or**
  - Authentication checks inside views
- Unauthorized users are redirected to the login page

---

## Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone https://github.com/adityadubey381/tweet-app-django.git
cd tweet-app-django
````

---

### 2️⃣ Create & activate virtual environment

```bash
python -m venv .venv
```

**Windows**

```bash
.venv\Scripts\activate
```

**Mac/Linux**

```bash
source .venv/bin/activate
```

---

### 3️⃣ Install dependencies

```bash
pip install django
```

(Optional)

```bash
pip freeze > requirements.txt
```

---

### 4️⃣ Apply migrations

```bash
python manage.py migrate
```

---

### 5️⃣ Create superuser (for admin access)

```bash
python manage.py createsuperuser
```

---

### 6️⃣ Run the development server

```bash
python manage.py runserver
```

---

## Application Routes

| URL              | Description                   |
| ---------------- | ----------------------------- |
| `/admin/`        | Django admin panel            |
| `/tweet/`        | Tweet homepage                |
| `/login/`        | User login                    |
| `/logout/`       | User logout                   |
| `/tweet/create/` | Create tweet (login required) |

---

## Access Rules

* ❌ Unauthenticated users cannot create tweets
* ✅ Authenticated users can create and add tweets
* 🔐 Django handles session-based authentication

---

## Learning Objectives

* Implement Django authentication
* Protect routes using authorization
* Understand login-required views
* Practice real-world Django project structure
* Proper Git & GitHub workflow

---

## Author

**Aditya Kumar Dubey**
GitHub: [https://github.com/adityadubey381](https://github.com/adityadubey381)
LinkedIn: [https://www.linkedin.com/in/aditya-kumar-dubey-9833b4278/](https://www.linkedin.com/in/aditya-kumar-dubey-9833b4278/)


