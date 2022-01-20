# Simple ToDo List with authorization on Python using Django

### Installation
Copy from source
```bash
git clone https://github.com/onlinegxd/pythonDjangoAssignment1
```

### Usage

```python
# Login/Register system
from django.contrib.auth.views import LoginView
from django.contrib.auth.mixins import LoginRequiredMixin
from django.contrib.auth.forms import UserCreationForm
from django.contrib.auth import login
# For views creation and redirects
from django.shortcuts import render, redirect
from django.views.generic.list import ListView
from django.views.generic.detail import DetailView
from django.views.generic.edit import CreateView, UpdateView, DeleteView, FormView
from django.urls import reverse_lazy
# For path through webpages
from django.urls import path
```

### Examples

Login with your account details or register a new account

After successful authorization you will able to create new tasks for current user

It's possible to edit/delete a task if it's needed

Database used is PostgreSQL

The main model in Database is Task model

Task
|     user              |      title        |       description        | complete     | created   |
| user who manages task | title of the task | description of the task  | True/False   | timestamp |

When the new Task is provided, user(current user) and created(timestamp) fields are filled automatically.


Usage examples:

(/login) - Route containing login form
If provided Login and Password are correct redirects us to -> (/) main page
![image](https://user-images.githubusercontent.com/80266425/150394067-68b1e35a-513c-444a-8826-5f6274004116.png)
![image](https://user-images.githubusercontent.com/80266425/150394178-061e7001-f52f-4a8d-909c-95718e074e5e.png)
If trying to access any pages without authorization redirects to authorization page

If provided user is not found outputs following text
![image](https://user-images.githubusercontent.com/80266425/150394246-82306b18-c87c-41d4-a38b-d1467748515f.png)

(/register) - Route for creating a new user
![image](https://user-images.githubusercontent.com/80266425/150394929-d7207e81-988b-4506-9932-7de47fd375d1.png)


(/) - Route table of tasks
![image](https://user-images.githubusercontent.com/80266425/150394367-bebb444e-abff-48ee-b12a-94ffd55ce77b.png)

(/task-create) - Route for creating tasks
![image](https://user-images.githubusercontent.com/80266425/150394444-ee846a32-3df7-4dfd-8c3a-2056acf81b84.png)

(/task-update/%task.id%/) - Route for updating tasks
![image](https://user-images.githubusercontent.com/80266425/150394608-2ec53721-378b-49a6-89a1-ab13347e1dcb.png)

(/task-delete/%task.id%/) - Route for deleting tasks
![image](https://user-images.githubusercontent.com/80266425/150394709-bd5ccd57-ac4a-4bb8-93fa-96c722d40677.png)


