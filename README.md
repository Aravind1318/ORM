# Ex02 Django ORM Web Application
# Date:
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
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

## models.py
```
from django.db import models
from django.contrib import admin

class Loan(models.Model):
    loan_id = models.AutoField(primary_key=True)
    customer_name = models.CharField(max_length=100)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
    interest_rate = models.DecimalField(max_digits=5, decimal_places=2)
    loan_term = models.IntegerField()
    disbursement_date = models.DateField()

class LoanAdmin(admin.ModelAdmin):
list_display=('loan_id','customer_name','loan_amount','interest_rate','loan_term','disbursement_date')
```
## admin.py
```
from django.contrib import admin
from .models import Loan,LoanAdmin

admin.site.register(Loan,LoanAdmin)
```
# ER DIAGRAM:
![image](https://github.com/user-attachments/assets/088d4bff-2f23-46e2-9973-daf0c22873f7)

# OUTPUT
![image](https://github.com/user-attachments/assets/26e27267-6385-410b-aa3d-02b0679d9585)


![image](https://github.com/user-attachments/assets/533e8bc2-8ec7-4762-bab8-69662e995e26)

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
