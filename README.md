# django-react-todo
## Description
A simple todo app built with Django Rest Framework and React.js

## Setup
### Backend
#### Requirements
- Python
- pip
- virtualenvwrapper
#### Installation
- Create a new virtual environment
```bash
$ mkvirtualenv django-react-todo
```
- Create a `backend` directory and go to it
```bash
$ mkdir backend && cd backend
```
- Create requirements.txt and add the following
    ```
    Django>=4.2.7,<4.3
    djangorestframework>=3.14.0,<3.15
    django-cors-headers>=4.3.1,<4.4
    ```
- Install requirements
```bash
$ pip install -r requirements.txt
```
- Create a new Django project
```bash
$ django-admin startproject backend .
```
- Add the following to `settings.py`
    ```python
    INSTALLED_APPS = [
        ...
        'rest_framework',
        'corsheaders',
    ]

    MIDDLEWARE = [
        ...
        'corsheaders.middleware.CorsMiddleware',
    ]

    CORS_ORIGIN_WHITELIST = [
        'http://localhost:3000'
    ]
    ```
- Migrate the database
```bash
$ python manage.py migrate
```
- Start the server
```bash
$ python manage.py runserver
```

