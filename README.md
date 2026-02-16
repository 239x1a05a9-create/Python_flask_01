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

Base URL: http://127.0.0.1:5000

AUTHENTICATION APIs

Login
Endpoint: POST /login
Content-Type: application/x-www-form-urlencoded

Request Body:
username=admin
password=1234

Response:

Redirects to / on success

Returns "Invalid credentials" on failure

Logout
Endpoint: GET /logout

Response:

Clears session

Redirects to /login

NOTES APIs

Get All Notes
Endpoint: GET /
Authentication Required: Yes

Response:

Returns HTML page displaying all notes

Add Note
Endpoint: POST /add
Content-Type: application/x-www-form-urlencoded

Request Body:
note=This is my note

Response:

Saves note to database

Redirects to /

Edit Note
Endpoint: POST /edit/<id>
Example: POST /edit/1

Request Body:
note=Updated note text

Response:

Updates note

Redirects to /

Delete Note
Endpoint: GET /delete/<id>
Example: GET /delete/1

Response:

Deletes note

Redirects to /

JSON API

Add Numbers API
Endpoint: POST /addNum
Content-Type: application/json

Request Body (JSON):
{
"num1": 10,
"num2": 20
}

Response (JSON):
{
"num1": 10,
"num2": 20,
"sum": 30
}


<img width="478" height="244" alt="image_1" src="https://github.com/user-attachments/assets/a0d5e517-ef50-42b1-b574-e6afb8decb0d" />
<img width="436" height="230" alt="image_2" src="https://github.com/user-attachments/assets/d6f194cb-216a-4d7b-b05f-c765e4609e6a" />


