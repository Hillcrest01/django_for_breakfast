

## Introduction

**Django** is a high-level Python web framework that encourages rapid development and clean, pragmatic design.
It follows the **Model-Template-View (MTV)** architectural pattern and is maintained by the Django Software Foundation.

Django is used for building web applications of all sizes—from small personal projects to large enterprise-level platforms.
It is known for its focus on **security**, **scalability**, and **maintainability**.

---

## Prerequisites

* Ensure **Python** is installed on your system.
* Then install Django using:

```bash
pip install django
```

---

## Verify Django Installation

Open a Python shell:

```bash
python
```

Then at the Python prompt, run:

```python
>>> import django
>>> print(django.get_version())
```

If the Django version prints successfully, Django is installed correctly.
If you receive an error, reinstall Django.

---

## Creating Your First Django Project

1. Create a project directory:

```bash
mkdir djangotutorial
```

2. Bootstrap a new Django project:

```bash
django-admin startproject mysite djangotutorial
```

Or (alternative):

```bash
python -m django startproject mysite djangotutorial
```

This will create the following structure:

```
djangotutorial/
├── manage.py
└── mysite/
    ├── __init__.py
    ├── asgi.py
    ├── settings.py
    ├── urls.py
    └── wsgi.py
```

### File Descriptions

* **manage.py** – Command-line utility for interacting with the project.
* **mysite/** – Project package containing the actual Django app code.

  * ****init**.py** – Marks the directory as a Python package.
  * **settings.py** – Project settings and configuration.
  * **urls.py** – URL declarations (acts like a site table of contents).
  * **asgi.py** – ASGI server entry point (for async support).
  * **wsgi.py** – WSGI server entry point (used for deployment).

---

## Running the Development Server

Navigate to the project directory:

```bash
cd djangotutorial
```

Start the development server:

```bash
python manage.py runserver
```

Expected output:

```
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C
```

If the server starts successfully, you're good to go!
If not, revisit the previous steps to ensure everything is properly set up.

