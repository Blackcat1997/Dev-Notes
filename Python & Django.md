# Django Basic
## What is Django?
Django is a web framework — a set of tools designed to help you build interactive websites.  

## Before building websites
### Spec  
Writing a spec to Introduce the project details.

### Virtual Environment
**What is a virtual environment?**  
A virtual environment is a place on your system where you can install packages and isolate them from all other Python packages.  

**Implementing Steps**

1. Create: Go to the project directory, then run the command  
`python -m virtualenv new_env`  
2. Activate   
`source new_env/bin/activate`  
3. Deactive  
`deactive`

### Django
* **Installing:** *Without leaving the active virtual environment.*  
`pip install Django`  

* **Creating a Project**  
`django-admin.py startproject new-project .`(*Dot creates the new project with a directory*)

* **Creating the Database**  
`python manage.py migrate`  

* **Viewing the Project**  
`python manage.py runserver`

# APP
## Creating a new app
A Django project is organized as a group of individual apps that work together to make the project work as a whole.
### How to create apps?
1. Run `runserver` command  
2. Activate the virtual env  
3. Run `startapp` command to create a new app folder
	* admin.py
	* models.py
	* views.py
## Models
### Defining Models
* Defining models (creating classes) is equivalent to create tables in SQL.  
* A model tells Django how to work with the data that will be stored in the app.
### activating models
To user the models we define, we have to tell Django to include the app in the overall.  
1. Open (project folder)/settings.py  

```
INSTALLED_APPS = (  
	--snip--    
	'django.contrib.staticfiles', 
	   
	# New apps    
	'the App name',  
)
```  

### Modifing the database  
Every time after we added a new model, we need to migrate the database.  

**How to migrate the database?** *(Two steps)* 
 
1. Migrate the database and check the output  
`python manage.py make migrations`  

2. Apply the migration  
`python manage.py migrate`

### Registering the models
**admin.py**  

```
from (app folder).models import (new_class)

admin.site.register(new_class_name)
```

### The Django Shell
* Django shell is an interactive environment for testing and troubleshooting.  
`python manage.py shell`

* The shell is very useful for making sure the code retrieves the data you want it to.  

## Making Pages
### Three stages
* Defining URLs  
* Writing Views  
* Writing templates

### URL
Users request pages by entering URLs into a browser and clicking links.  

**First** 
 
* Define patterns for URLs.  
A URL pattern describes the way the URL is laid out and tells Django what to look for when matching a browser request with a site URL so it knows which page to return.  
 
**Base URL**  

* Including folders&files:  
	* project folder/urls.py   
	* app folder  

1. Modify the urls.py in the project folder  
		*In this urls.py file, which represents the projects as a whole, which sets of URLs from the apps in the project.*

	```
		urlpatterns = [
				--snip--
				path('', include('app_folder.urls'))
		]
	```

2. Create a new urls.py file in the app folder  

	```
	from django.urls import path
	from . import views
	
	app_name = 'learning_logs'
	urlpatterns = [
			# Home page
			path('', views.index, name='index'),
	]
	```

3. Writing a View  

	* app folder/views.py      

4. Writing a Template  

	* index.html
5. Project folder/setting.py  

	```
	TEMPLATES {  
		--snip--
		
		'DIRS': [os.path.join(BASE_DIR, '')]  
		
		--snip--
	}
	```
