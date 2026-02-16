Flask Notes App
A simple Notes Management Web Application built with Flask and SQLite. This app allows users to log in, create, edit, and delete notes. It also includes a basic JSON API endpoint for adding numbers.

Features

User authentication (Login / Logout)
Create, view, edit, and delete notes
SQLite database integration using SQLAlchemy
Session-based authentication
REST API endpoint for adding numbers
Automatic database initialization with default admin user

Tech Stack

Python 3.x
Flask
Flask-SQLAlchemy
SQLite
Gunicorn (for production deployment)

Installation

1. Clone the repository
git clone https://github.com/239x1a05a9-create/Python_flask_01.git
cd flask-notes-app
2. Create virtual environment
python -m venv venv
Activate it:
Windows
venv\Scripts\activate
Linux / Mac
source venv/bin/activate

API Endpoints

Base URL:

http://127.0.0.1:5000
Authentication APIs
Login

Endpoint

POST /login

Content-Type

application/x-www-form-urlencoded

Request Body

username=admin
password=1234

Response

Redirects to / on success

Returns error message on failure

Logout

Endpoint

GET /logout

Response

Redirects to /login
Notes APIs
Get All Notes

Endpoint

GET /

Auth Required: Yes

Response

Returns HTML page displaying all notes
Add Note

Endpoint

POST /add

Content-Type

application/x-www-form-urlencoded

Request Body

note=This is my note

Response

Redirects to /
Edit Note

Endpoint

POST /edit/<id>

Example

POST /edit/1

Request Body

note=Updated note text

Response

Redirects to /
Delete Note

Endpoint

GET /delete/<id>

Example

GET /delete/1

Response

Redirects to /
JSON API
Add Numbers API

Endpoint

POST /addNum

Content-Type

application/json

Request Body

{
  "num1": 10,
  "num2": 20
}

Response

{
  "num1": 10,
  "num2": 20,
  "sum": 30
}
