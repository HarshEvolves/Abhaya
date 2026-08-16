# Abhaya

**Abhaya** is a safety-focused mobile application designed to provide users with quick access to emergency assistance, trusted contacts, authentication, and essential personal safety features.

## 🚀 Overview

Abhaya aims to make emergency assistance simple and accessible through a single mobile application.

The application provides a secure flow for:

* User registration and authentication
* Personal information management
* Trusted emergency contacts
* Emergency assistance workflows
* Secure backend APIs
* Persistent PostgreSQL database storage

## 🏗️ Architecture

```text
┌─────────────────────┐
│    Flutter Mobile   │
│        App          │
└──────────┬──────────┘
           │ REST API
           ▼
┌─────────────────────┐
│      FastAPI        │
│      Backend        │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│     PostgreSQL      │
│      Database       │
└─────────────────────┘
```

## 🛠️ Tech Stack

### Frontend

* Flutter
* Dart

### Backend

* Python
* FastAPI
* SQLAlchemy
* Alembic
* JWT Authentication

### Database

* PostgreSQL

### Development Tools

* Git
* GitHub
* Docker
* REST APIs

## 📁 Project Structure

```text
Abhaya/
│
├── backend/
│   ├── app/
│   ├── alembic/
│   ├── tests/
│   ├── requirements.txt
│   └── ...
│
├── mobile/
│   ├── lib/
│   ├── android/
│   ├── ios/
│   ├── pubspec.yaml
│   └── ...
│
├── .gitignore
└── README.md
```

> The exact structure may vary depending on the current implementation.

## 🔐 Core Features

### Authentication

* User registration
* Login
* Secure authentication
* JWT-based authorization

### Personal Information

* User profile management
* Secure storage of user information
* Update profile information

### Trusted Contacts

* Add trusted emergency contacts
* Update contact information
* Remove contacts
* Associate contacts with the authenticated user

### Emergency Assistance

* Emergency-focused application workflow
* Quick access to safety-related functionality
* Backend support for emergency operations

## 🗄️ Database

Abhaya uses **PostgreSQL** for persistent data storage.

Database schema changes are managed using **Alembic migrations**.

Example:

```bash
alembic upgrade head
```

## ⚙️ Backend Setup

Clone the repository:

```bash
git clone https://github.com/HarshEvolves/Abhaya.git
cd Abhaya/backend
```

Create a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Configure environment variables:

```bash
cp .env.example .env
```

Update the `.env` file with your local PostgreSQL and authentication configuration.

Run database migrations:

```bash
alembic upgrade head
```

Start the FastAPI server:

```bash
uvicorn app.main:app --reload
```

The API will be available at:

```text
http://127.0.0.1:8000
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

## 📱 Mobile Setup

Navigate to the Flutter application:

```bash
cd mobile
```

Install dependencies:

```bash
flutter pub get
```

Check connected devices:

```bash
flutter devices
```

Run the application:

```bash
flutter run
```

## 🔄 Development Workflow

```text
Flutter UI
    ↓
FastAPI REST API
    ↓
Service / Business Logic
    ↓
SQLAlchemy
    ↓
PostgreSQL
```

Database schema changes are handled through:

```text
Alembic → PostgreSQL
```

## 🔒 Security

The project is designed with security in mind.

* JWT-based authentication
* Protected API endpoints
* User-specific data access
* Environment variables for sensitive configuration
* PostgreSQL persistence
* Secrets excluded from version control

**Never commit `.env` files, API keys, passwords, or other secrets to GitHub.**

## 🧪 Testing

Backend tests can be executed using:

```bash
pytest
```

Flutter tests can be executed using:

```bash
flutter test
```

## 📌 Project Status

**Status:** Active Development

The project is currently being developed with the Flutter frontend and FastAPI/PostgreSQL backend being integrated into a complete safety application.

## 👨‍💻 Author

**Harsh Kukutkar**

GitHub: [HarshEvolves](https://github.com/HarshEvolves)

## 📄 License

This project is currently intended for development and educational purposes.
