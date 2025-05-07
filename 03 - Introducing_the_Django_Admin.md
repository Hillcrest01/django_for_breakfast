
### Creating an Admin User in Django

To create an admin user in Django, follow these steps:

1. Run the following command:

   ```bash
   python manage.py createsuperuser
   ```

   You will be prompted to enter a **username**, **email address**, and **password**.

2. Start the development server:

   ```bash
   python manage.py runserver
   ```

3. Open your browser and go to:

   ```
   http://localhost:8000/admin
   ```

   You will be able to log in using the superuser credentials you just created.

---

### Registering the Polls App in the Admin Panel

By default, your `polls` app and its models will not appear in the admin panel until you register them.

To register the `Questions` model:

1. Open the file `polls/admin.py`.

2. Add the following code:

   ```python
   from django.contrib import admin
   from .models import Questions

   admin.site.register(Questions)
   ```

Now, when you visit the admin panel, you’ll see the `Questions` model listed and can perform full **CRUD (Create, Read, Update, Delete)** operations on its data.

---

