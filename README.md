# Ex02 Django ORM Web Application
# Date:
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM

![image](https://github.com/user-attachments/assets/de4a159f-3f41-4b5d-b422-eeae34edca0e)

## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
```
from django.db import models

class bankloan(models.Model):
    loan_id = models.AutoField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=20)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
    loan_term = models.IntegerField()
    interest_rate = models.DecimalField(max_digits=5, decimal_places=2)
```
```
from django.contrib import admin
from .models import bankloan

class BankLoanAdmin(admin.ModelAdmin):
    list_display = ('loan_id', 'customer_name', 'account_type', 'loan_amount', 'loan_term', 'interest_rate')
    list_filter = ('account_type', 'loan_term')
    search_fields = ('customer_name', 'account_type')

admin.site.register(bankloan, BankLoanAdmin)
```
# OUTPUT
Include the screenshot of your admin page.

![image](https://github.com/user-attachments/assets/70809b15-4302-4610-b138-f59590f85502)

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
