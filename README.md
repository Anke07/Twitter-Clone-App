# Twitter Clone App

A beginner-friendly social media web application built with Python and Django.
Users can register, sign in, publish short posts, edit or delete their own posts,
like and unlike posts, and view user profiles.

## Features
- User registration, login and logout
- Create, edit and delete your own posts
- Like and unlike posts
- Home feed ordered by newest posts
- User profile pages with post history
- Responsive layout with plain HTML and CSS
- SQLite database for local development

## Tech stack
- Python 3.10+
- Django 5.2
- SQLite
- HTML5 and CSS3

## Run locally

1. Install Python 3.10 or newer.
2. Open a terminal in this project folder.
3. Create and activate a virtual environment:

   Windows:
   ```bash
   py -m venv venv
   venv\Scripts\activate
   ```

   macOS/Linux:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

4. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Create the database tables:

   ```bash
   python manage.py migrate
   ```

6. Start the development server:

   ```bash
   python manage.py runserver
   ```

7. Open http://127.0.0.1:8000/ in your browser and create an account.

## Project structure

```text
twitter_clone_app/
├── manage.py
├── requirements.txt
├── README.md
├── .gitignore
├── twitter_clone/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
└── tweets/
    ├── __init__.py
    ├── admin.py
    ├── apps.py
    ├── forms.py
    ├── models.py
    ├── urls.py
    ├── views.py
    ├── migrations/
    │   └── __init__.py
    ├── templates/
    │   └── tweets/
    │       ├── base.html
    │       ├── home.html
    │       ├── form.html
    │       ├── login.html
    │       ├── register.html
    │       └── profile.html
    └── static/
        └── tweets/
            └── style.css
```

## Notes
- This is a learning/demo project. It uses Django's local development server
  and SQLite by default.
- Do not deploy with `DEBUG=True` or the development `SECRET_KEY`.
- Before public deployment, configure environment-based secrets, HTTPS,
  allowed hosts, production database, static files and hosting.
- The project does not use the Twitter/X API and is not affiliated with X.

## Future improvements
- Profile pictures and editable bios
- Image uploads
- Follow/unfollow users
- Search and pagination
- Automated tests
