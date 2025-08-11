---

MyJournal

MyJournal is a personal journal web application designed to help users securely record, manage, and reflect on their daily thoughts, ideas, and experiences. This project is my submission for the CS50x 2025 Final Project. It is built using Python (Flask) for the backend and SQLite for data storage, with HTML and CSS templates for the frontend.

The application enables users to register for an account, log in securely, and manage journal entries by adding, editing, and deleting them. Every user's data is kept private, and passwords are stored in a hashed form to ensure security.


---

Project Purpose and Inspiration

The inspiration behind MyJournal came from the need for a simple, lightweight, and private online journaling tool. Many existing note-taking or journaling platforms are overly complex or require users to share data with external servers. My goal was to create something minimal, easy to use, and entirely under the user's control.

As part of the CS50 Final Project, I wanted to combine concepts learned in the course — such as Flask routing, SQL queries, user authentication, HTML templates, and session handling — into one functional web application.


---

Features

MyJournal has the following core features:

1. User Registration and Login

New users can create an account by providing a unique username and password.

Passwords are hashed using Werkzeug before being stored in the database, ensuring that sensitive data is never saved in plain text.

Returning users can log in securely and access only their own journal entries.



2. Add Journal Entries

Once logged in, users can write new journal entries.

Each entry can have a title and body text, and the date is recorded automatically.



3. Edit Existing Entries

Users can modify the title or content of their existing entries to make corrections or updates.



4. Delete Journal Entries

If a user no longer wants an entry, they can permanently remove it from the database.



5. View All Entries

The homepage displays all of the user's entries in reverse chronological order (latest first).



6. SQLite Database Backend

The application uses a lightweight SQLite database for storing user accounts and journal entries.

All data is stored locally, giving users complete control.





---

Technologies Used

Python – Backend logic, form handling, and authentication.

Flask – Web framework for routing, template rendering, and session management.

SQLite – Local relational database for storing user and journal data.

HTML & CSS – Frontend structure and styling.

Werkzeug Security – For password hashing and verification.



---

How to Run Locally

1. Install dependencies

pip install -r requirements.txt


2. (Optional) Initialize the database
If running for the first time, create a fresh database:

flask init-db


3. Run the application

flask run


4. Access in your browser
Go to:

http://127.0.0.1:5000


5. Register and start journaling!




---

Folder Structure

myjournal/
├── app.py
├── journal.db
├── requirements.txt
├── README.md
└── templates/
    ├── login.html
    ├── register.html
    ├── index.html
    ├── add.html
    └── edit.html


---

Development Process

I followed a step-by-step process to build MyJournal:

1. Planning the Database

Created a users table for storing user credentials.

Created an entries table for storing journal entries linked to a specific user ID.



2. User Authentication

Implemented /register and /login routes.

Added session management to keep users logged in.



3. Journal Functionality

Added /add, /edit/<id>, and /delete/<id> routes.

Used SQL queries to fetch and update entries.



4. Frontend Design

Created HTML templates for each page.

Added simple CSS for readability and user experience.



5. Testing

Tested all routes for functionality.

Ensured that users cannot access each other’s entries.





---

Challenges Faced

User Authentication Logic – Making sure sessions worked correctly without exposing private data.

Database Relationships – Linking entries to specific users required careful SQL queries.

Error Handling – Ensuring the app returned friendly messages when something went wrong.

Minimal but Functional UI – Balancing simplicity with usability was a key consideration.



---

Lessons Learned

Through this project, I strengthened my understanding of:

Flask routing and template rendering.

SQL query writing and database design.

Password hashing and secure authentication.

Organizing a Flask project for readability.



---

Future Improvements

If I continue developing MyJournal, I would like to add:

Search and Tagging – So users can quickly find specific entries.

Rich Text Editor – To allow bold, italic, and other formatting in journal entries.

Export to PDF – Let users download their journals for offline storage.

Mobile-Friendly UI – Improve responsiveness for phone and tablet users.



---

Demo Video

Watch on YouTube: https://youtu.be/VzlRnyzc1kw


---

GitHub Repository

https://github.com/BijoyMojumder200/myjournal


---

Author

Bijoy Mojumder
CS50 Final Project – 2025
City & Country: Noakhali, Bangladesh
edX Username: b-mojumder


---
