# Simon's Rock Housing Database

A comprehensive, full-stack Database Management System engineered specifically for Bard College at Simon's Rock. This application provides a secure and dynamic platform to manage, organize, and query complex college housing data.

## What It Does

At its core, this application translates raw relational database information into an intuitive, accessible web interface. 

* **Secure Access:** Users navigate through a secure authentication pipeline to access the system, ensuring data privacy and role-based access.
* **Personalized Dashboards:** The system generates personalized multi-page views tailored to the user, displaying relevant housing assignments, dormitory capacities, and student profiles.
* **Dynamic Data Querying:** Users can perform complex searches—such as filtering students by housing status or identifying available beds in specific dorms—without needing to write a single line of SQL. The frontend intuitively translates user inputs into complex backend queries and renders the results dynamically.

## How It Works

This project leverages the Django web framework to bridge a highly structured SQLite database with a responsive frontend.

* **Strict Relational Architecture:** The backend database is built on a fully normalized relational schema to eliminate data redundancy. It utilizes complex foreign keys to establish strict, logical relationships between students, rooms, and dormitories.
* **Automated Data Integrity:** To prevent data anomalies (such as overbooking a room or creating orphaned student records), the database employs custom automated triggers and indexing. This enforces strict business logic at the lowest level, making the system highly reliable.
* **Dynamic Rendering:** The application uses Django's templating engine to generate HTML pages on the fly. JavaScript and CSS are layered on top to create a responsive user interface that updates seamlessly based on the SQLite data. Furthermore, Django's built-in session management is utilized to preserve user states across different pages safely.

## Tech Stack

* **Backend:** Python, Django Web Framework
* **Database:** SQLite (Custom automated triggers, indexing, and foreign key constraints)
* **Frontend:** HTML5, CSS3, Vanilla JavaScript, Django Templates

## Getting the Code

To view the source code locally, simply clone the repository:

```bash
git clone [https://github.com/jackb-22/Housing-Database.git](https://github.com/jackb-22/Housing-Database.git)
```
