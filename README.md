# Simon's Rock Housing Database

A Django-based housing management system for organizing and querying college housing data. The app provides a web interface for viewing students, rooms, buildings, leases, room availability, and community director assignments.

## Live Demo

Live demo: https://jsb2302.pythonanywhere.com/

Demo admin login:

```text
Username: demo_admin
Password: demo123
```

Demo community director login:

```text
Username: Taylor Demo
Password: 10001
```

This public deployment uses sanitized demo data only.

## What It Does

This project turns relational housing data into an interactive web application. Instead of manually querying the database, users can log in and navigate through dashboards that display housing assignments, dorm capacity, student records, room availability, and lease information.

Key features include:

- Role-based login flow for admin users and community directors
- Admin dashboard for viewing and managing housing-related records
- Community director views filtered to relevant building and room data
- Search and query functionality for students, rooms, leases, and housing status
- SQLite-backed relational data model connecting students, rooms, buildings, leases, and community directors
- Dynamic HTML rendering using Django templates

## Tech Stack

- **Backend:** Python, Django
- **Database:** SQLite
- **Frontend:** HTML, CSS, JavaScript, Django Templates
- **Deployment:** PythonAnywhere

## Project Structure

```text
Housing-Database/
└── housing/
    └── finalprj/
        ├── manage.py
        ├── db.sqlite3
        ├── finalprj/
        │   ├── settings.py
        │   ├── urls.py
        │   └── wsgi.py
        └── housingapp/
            ├── models.py
            ├── views.py
            ├── urls.py
            └── templates/
```

The main Django project is located in:

```text
housing/finalprj/
```

## Running Locally

Clone the repository:

```bash
git clone https://github.com/jackb-22/Housing-Database.git
cd Housing-Database/housing/finalprj
```

Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

Install dependencies:

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

Run migrations:

```bash
python manage.py migrate
```

Start the development server:

```bash
python manage.py runserver
```

Then open:

```text
http://127.0.0.1:8000/
```
and utilize the same credentials as the live demo.

## Database Model

The application uses a relational SQLite schema with the following core entities:

- **Building** — stores dorm/building information
- **Room** — stores room number, capacity, status, and building assignment
- **Student** — stores student records
- **Lease** — links students to room assignments over a date range
- **CommunityDirector** — links staff users to assigned buildings

These models are connected through Django foreign keys, allowing the app to query housing relationships across students, rooms, buildings, and leases.

## Deployment Notes

The live version is deployed on PythonAnywhere using:

- Django application served through WSGI
- SQLite database with sanitized demo data
- Static files collected for production use
- `DEBUG = False` for the public deployment
