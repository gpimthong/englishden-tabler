# [Django Dashboard Tabler](https://appseed.us/admin-dashboards/django-dashboard-tabler)

Open-source **[Django Dashboard](https://appseed.us/admin-dashboards/django)** generated by AppSeed op top of an iconic design. **Tabler** is a open-source admin template crafted by Codecalm agency. It comes with the basic components and set of pre-built pages required to lay the foundation for any application - Design provided by Codecalm.

- 👉 [Django Tabler](https://appseed.us/admin-dashboards/django-dashboard-tabler) - product page
- 👉 [Django tabler](https://django-dashboard-tabler.appseed.us/) - LIVE App

<br />

## [Black Friday](https://appseed.us/discounts/) - `75%OFF`

> The campaign is active until `30.NOV` and applies to all products and licenses.

[![AppSeed - Black Friday 2022 Campaign, 75% OFF Discount (all products).](https://user-images.githubusercontent.com/51070104/201829599-9fe6bdd7-3f19-46f3-9115-962eeb13bf29.jpg)](https://appseed.us/discounts/)

<br />

> Features

- `Up-to-date dependencies`
- UI-Ready app, `SQLite Database`, Django Native ORM
- `Session-Based authentication`, Forms validation
- `Deployment`: **Docker**, Gunicorn / Nginx, HEROKU
- Support via **Github** (issues tracker) and [Discord](https://discord.gg/fZC6hup).

<br />

![Django Dashboard Tabler - Open-Source Dashboard.](https://user-images.githubusercontent.com/51070104/202659663-fbb0ed51-677a-43fe-ad0b-13aaf5bd495b.png)

<br />

## ✨ Quick Start in `Docker`

> Get the code

```bash
$ git clone https://github.com/app-generator/django-tabler.git
$ cd django-tabler
```

> Start the app in Docker

```bash
$ docker-compose up --build
```

Visit `http://localhost:85` in your browser. The app should be up & running.

<br />

![Django Dashboard Tabler - Open-Source Web App.](https://raw.githubusercontent.com/app-generator/static/master/products/django-dashboard-tabler-screen.png)

<br />

## ✨ How to use it

```bash
$ # Get the code
$ git clone https://github.com/app-generator/django-tabler.git
$ cd django-tabler
$
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv env
$ source env/bin/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv env
$ # .\env\Scripts\activate
$ 
$ # Install modules
$ # SQLIte version
$ pip3 install -r requirements.txt
$
$ # Create tables
$ python manage.py makemigrations
$ python manage.py migrate
$
$ # Start the application (development mode)
$ python manage.py runserver # default port 8000
$
$ # Start the app - custom port 
$ # python manage.py runserver 0.0.0.0:<your_port>
$
$ # Access the web app in browser: http://127.0.0.1:8000/
```

<br />

## ✨ Code-base structure

The project is coded using a simple and intuitive structure presented bellow:

```bash
< PROJECT ROOT >
   |
   |-- core/                                # Implements app configuration
   |    |-- settings.py                     # Defines Global Settings
   |    |-- wsgi.py                         # Start the app in production
   |    |-- urls.py                         # Define URLs served by all apps/nodes
   |
   |-- apps/
   |    |
   |    |-- home/                           # A simple app that serve HTML files
   |    |    |-- views.py                   # Serve HTML pages for authenticated users
   |    |    |-- urls.py                    # Define some super simple routes  
   |    |
   |    |-- authentication/                 # Handles auth routes (login and register)
   |    |    |-- urls.py                    # Define authentication routes  
   |    |    |-- views.py                   # Handles login and registration  
   |    |    |-- forms.py                   # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>          # CSS files, Javascripts files
   |    |
   |    |-- templates/                      # Templates used to render pages
   |         |-- includes/                  # HTML chunks and components
   |         |    |-- navigation.html       # Top menu component
   |         |    |-- sidebar.html          # Sidebar component
   |         |    |-- footer.html           # App Footer
   |         |    |-- scripts.html          # Scripts common to all pages
   |         |
   |         |-- layouts/                   # Master pages
   |         |    |-- base-fullscreen.html  # Used by Authentication pages
   |         |    |-- base.html             # Used by common pages
   |         |
   |         |-- accounts/                  # Authentication pages
   |         |    |-- login.html            # Login page
   |         |    |-- register.html         # Register page
   |         |
   |         |-- home/                      # UI Kit Pages
   |              |-- index.html            # Index page
   |              |-- 404-page.html         # 404 page
   |              |-- *.html                # All other pages
   |
   |-- requirements.txt                     # Development modules - SQLite storage
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- manage.py                            # Start the app - Django default start script
   |
   |-- ************************************************************************
```

<br />

> The bootstrap flow

- Django bootstrapper `manage.py` uses `core/settings.py` as the main configuration file
- `core/settings.py` loads the app magic from `.env` file
- Redirect the guest users to Login page
- Unlock the pages served by *app* node for authenticated users

<br />

## ✨ Deployment

The app is provided with a basic configuration to be executed in [Docker](https://www.docker.com/), [Gunicorn](https://gunicorn.org/), and [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/).

### [Gunicorn](https://gunicorn.org/)
---

Gunicorn 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.

> Install using pip

```bash
$ pip install gunicorn
```
> Start the app using gunicorn binary

```bash
$ gunicorn --bind=0.0.0.0:8001 core.wsgi:application
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.


<br />

### [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/)
---

Waitress (Gunicorn equivalent for Windows) is meant to be a production-quality pure-Python WSGI server with very acceptable performance. It has no dependencies except ones that live in the Python standard library.

> Install using pip

```bash
$ pip install waitress
```
> Start the app using [waitress-serve](https://docs.pylonsproject.org/projects/waitress/en/stable/runner.html)

```bash
$ waitress-serve --port=8001 core.wsgi:application
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

## ✨ Credits & Links

- [Django](https://www.djangoproject.com/) - The official website
- [Boilerplate Code](https://appseed.us/boilerplate-code) - Index provided by **AppSeed**
- [Boilerplate Code](https://github.com/app-generator/boilerplate-code) - Index published on Github

<br />

---
[Django Dashboard Tabler](https://appseed.us/admin-dashboards/django-dashboard-tabler) - Provided by **AppSeed [App Generator](https://appseed.us/app-generator)**.
