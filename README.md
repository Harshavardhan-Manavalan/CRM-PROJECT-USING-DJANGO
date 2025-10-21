# CRM Project Using Django

## Overview
The Customer Relationship Management (CRM) project is developed using the Django framework with MySQL as the database. It enables users to perform CRUD operations—Add, View, Update, and Delete customer records—through a web interface with user authentication.

---

## Features
- User registration, login, and logout
- Add, update, delete, and view customer records
- Admin dashboard for managing data
- MySQL database integration using Django ORM
- Responsive interface built with HTML and Bootstrap

---

## Prerequisites
**Frontend:** HTML, Bootstrap  
**Backend:** Django  
**Database:** MySQL  

### Required Software
| Software | Version | Download Link |
|-----------|----------|----------------|
| Git | 2.43.0 | [git-scm.com](https://www.git-scm.com/download/win) |
| Visual Studio Code | 1.85.1 | [code.visualstudio.com](https://code.visualstudio.com/download) |
| MySQL Workbench | 8.0.34 | [mysql.com](https://dev.mysql.com/downloads/installer/) |

---

## Installation

### Step 1: Clone the Repository
```bash
git clone https://github.com/Harshavardhan-Manavalan/CRM-.git
cd CRM-
````

### Step 2: Install Dependencies

```bash
pip install django==3.2
pip install mysql-connector-python
```

### Step 3: Configure the Database

In `settings.py`:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'elderco',
        'USER': 'root',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

Run database migrations:

```bash
python manage.py makemigrations
python manage.py migrate
```

---

## Create a Superuser

```bash
python manage.py createsuperuser
```

---

## Run the Server

```bash
python manage.py runserver
```

* Main Page: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
* Admin Page: [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

---

## Code Flow Summary

1. User sends a request via browser.
2. Django routes it through `urls.py` to the respective view.
3. The view processes logic and interacts with the model.
4. Data is retrieved or saved to MySQL using ORM.
5. Response is rendered with HTML templates and returned to the user.

---

## Model Example

```python
class Record(models.Model):
    first_name = models.CharField(max_length=50)
    last_name = models.CharField(max_length=50)
    email = models.CharField(max_length=100)
    phone = models.CharField(max_length=15)
    address = models.CharField(max_length=100)
    city = models.CharField(max_length=50)
    state = models.CharField(max_length=50)
    zipcode = models.CharField(max_length=20)
```

---

## Summary

This Django CRM project demonstrates end-to-end functionality of a customer management system using Django MVC architecture and MySQL integration. It includes authentication, CRUD operations, and an admin interface for managing records efficiently.

---

**Author:** Harshavardhan Manavalan
**GitHub:** [Harshavardhan-Manavalan](https://github.com/Harshavardhan-Manavalan)

