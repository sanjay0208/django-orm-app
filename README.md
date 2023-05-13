# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
create a simple table using table tag

### STEP2:
add header row using the tag
### STEP 3:
add your timetable

### STEP 4:
execute the program

## PROGRAM
~~~
from django.db import models
from django.contrib import admin

class Student(models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    dept=models.CharField(max_length=5)


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','dept')
~~~
File:Admin.py
~~~
from django.contrib import admin
from .models import Student,StudentAdmin
admin.site.register(Student,StudentAdmin)
~~~
## OUTPUT
![slot time table](https://github.com/sanjay0208/django-orm-app/assets/119406959/4ff30c9a-ca58-4257-ad28-7adb80dd59a4)


## RESULT
A Django application has been created that can be used to store and retrieve data from the database using Object Relational Mapping(ORM).
