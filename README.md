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

### Frontend
#### Requirements
- Node.js
- npm
#### Installation
- Open a new terminal within the root directory
- Create a new React app
```bash
$ npx create-react-app frontend
```
- Go to the `frontend` directory and start the server
```bash
$ cd frontend
$ npm start
```
- Install bootstrap and reactstrap to provide user interface tools
```bash
$ npm install bootstrap@5.1.3 reactstrap@9.2.1
```
- Install axios to make HTTP requests to the API endpoints
```bash
$ npm install axios
```


## Credits
https://www.digitalocean.com/community/tutorials/build-a-to-do-application-using-django-and-react