### 🛠️ Setting Up the Polls App in Django

In Django, your apps can live anywhere in your Python path. For this tutorial, we’ll create the `polls` app inside the `djangotutorial` folder.

#### Step 1: Create the Polls App

Make sure you're in the same directory as `manage.py`, then run:

```bash
$ python manage.py startapp polls
```

This command will create a `polls/` directory that will contain the application code.

---

#### Step 2: Create the First View

Open the `polls/views.py` file, clear any existing code, and add the following:

```python
from django.http import HttpResponse

def index(request):
    return HttpResponse("Hello, world.")
```

---

#### Step 3: Create `polls/urls.py`

This file will map URLs specific to the `polls` app. Create a new file named `urls.py` inside the `polls` directory and add the following:

```python
from django.urls import path
from . import views

urlpatterns = [
    path("", views.index, name="index"),
    # This defines the root URL for the 'polls/' path.
]
```

---

#### Step 4: Configure the Main URLconf

Open `mysite/urls.py`. By default, it might look like this:

```python
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path("admin/", admin.site.urls),
]
```

Update it to include the `polls` app URLs:

```python
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path("polls/", include("polls.urls")),
    path("admin/", admin.site.urls),
]
```

Now, when you navigate to `http://localhost:8000/polls/`, you should see:
`Hello, world.`

---
