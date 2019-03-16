# Python & Django
## What is Django?
Django is a web framework — a set of tools designed to help you build interactive websites.  

## Before building websites
### Spec  
Writing a spec to Introduce the project details.

### Virtual Environment
* **What is a virtual environment?**  
A virtual environment is a place on your system where you can install packages and isolate them from all other Python packages.  

* **Step**  
1. Create  
Go to the project directory, then run the command  
`python -m virtualenv new_env`  
2. Activate   
`source new_env/bin/activate`   
3. Deactive  
`deactive`  

### Django
* **Installing**  
> *Without leaving the active virtual environment.*    
`pip install Django`  

* **Creating a Project**  
`django-admin.py startproject new-project .`  
> *Dot creates the new project with a directory*    

* **Creating the Database**  
`python manage.py migrate`  

* **Viewing the Project**  
`python manage.py rumserver`
