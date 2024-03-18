# Ex02 Django ORM Web Application
## Date: 11/03/2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![image (1)](https://github.com/jesu-smartia05/ORM/assets/148514819/9425b632-d0f5-4f91-92da-8bee02dc3795)

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
Models.py
```
from django.db import models
from django.contrib import admin
class Book_dbs(models.Model):
    BOOKNUM=models.IntegerField(primary_key="bookno");
    TITLE=models.CharField(max_length=25);
    AUTHOR=models.CharField(max_length=50);
    DATE=models.DateField();
    LANG=models.CharField(max_langth=20);
    PRICE=models.IntegerField();
class Book_dbsAdmin(admin.ModelAdmin):
    list_display=("BOOKNUM","TITLE","AUTHOR","DATE","LANG","PRICE");

```
Admin.py
```
from django.contrib import admin
from .models import Book_dbs,Book_dbsAdmin
admin.site.register(Book_dbs,Book_dbsAdmin)
```

## OUTPUT

![IMG-20240311-WA0010](https://github.com/jesu-smartia05/ORM/assets/148514819/e41d0402-382d-4f9e-b421-2dab6d0729a1)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
