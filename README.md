# ALX Travel App

A Django-based travel application with REST API support.

## Features

- REST API with Django REST Framework
- MySQL Database Integration
- CORS Headers Support
- Swagger API Documentation
- Celery for Asynchronous Tasks
- Redis for Caching and Message Broker

## Setup Instructions

### Prerequisites

- Python 3.8+
- MySQL Server
- Redis Server

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd alx_travel_app
```

2. Create and activate virtual environment:
```bash
python -m venv venv
# On Windows
venv\Scripts\activate
# On Unix or MacOS
source venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root (copy from `.env.example`):
```bash
cp .env.example .env
```

5. Update the `.env` file with your database credentials and other settings.

6. Create MySQL database:
```sql
CREATE DATABASE alx_travel_app_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

7. Run migrations:
```bash
python manage.py makemigrations
python manage.py migrate
```

8. Create a superuser:
```bash
python manage.py createsuperuser
```

9. Run the development server:
```bash
python manage.py runserver
```

## API Documentation

Once the server is running, you can access:

- **Swagger UI**: http://localhost:8000/swagger/
- **ReDoc**: http://localhost:8000/redoc/
- **Admin Panel**: http://localhost:8000/admin/

## Environment Variables

The following environment variables need to be configured in your `.env` file:

- `SECRET_KEY`: Django secret key
- `DEBUG`: Debug mode (True/False)
- `ALLOWED_HOSTS`: Comma-separated list of allowed hosts
- `DB_ENGINE`: Database engine (django.db.backends.mysql)
- `DB_NAME`: Database name
- `DB_USER`: Database user
- `DB_PASSWORD`: Database password
- `DB_HOST`: Database host
- `DB_PORT`: Database port

## Project Structure

```
alx_travel_app/
├── alx_travel_app/          # Project configuration
│   ├── settings.py          # Project settings
│   ├── urls.py              # URL configuration
│   ├── wsgi.py              # WSGI configuration
│   └── asgi.py              # ASGI configuration
├── listings/                # Listings app
├── manage.py                # Django management script
├── requirements.txt         # Python dependencies
├── .env.example             # Example environment variables
└── README.md                # This file
```

## Technologies Used

- **Django 5.2.7**: Web framework
- **Django REST Framework**: REST API toolkit
- **MySQL**: Database
- **drf-yasg**: Swagger/OpenAPI documentation
- **django-cors-headers**: CORS handling
- **Celery**: Asynchronous task queue
- **Redis**: Cache and message broker
- **django-environ**: Environment variable management

## License

This project is part of the ALX Software Engineering program.
