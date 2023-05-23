# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![orm](https://github.com/sanjay0208/django-orm-app/assets/119406959/2ea819ea-b737-4eb5-923c-c9b437e5cbf6)

Include your ER diagram here

## DESIGN STEPS
STEP 1:

Clone the problem from github
STEP 2:

create a new app
STEP 3:

Enter the codefor admin.py and model.py
Step 4:

Execute Django admin and create 10 employees


## PROGRAM
~~~
Model.py:

from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')
~~~

Admin.py:
~~~
from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)

~~~
## OUTPUT
![django orm](https://github.com/sanjay0208/django-orm-app/assets/119406959/11d5b9dd-6426-49d8-b234-5d7dacbeda00)



## RESULT
Thus a Django application to store and retrieve data from a database using Object Relational Mapping(ORM) is developed.
