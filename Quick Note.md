# QUICK NOTE
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

* project folder/urls.py   
* app folder/

1. Modify the urls.py in the project folder  
In this urls.py file, which represents the projects as a whole, which sets of URLs from the apps in the project.  

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
--- 
## Additional Pages
### Template Inheritance
* When building websites, you'll almost always require some elements to be repeated on each page.  
* Write a base template containing the repeated elements and then have each page inherit from the template.
### The Parent Template
**base.html**  

* This file contains elements common to all pages  
* Every other template inherit from *base.html*  

**Generating links**  

* We use a template tag, indicated by braces and percent sign {% %}.  
* A template tag is a bit of code that generates information to be displayed on a page.  
	
	```
	{% url '(project folder/urls.py/namespace):(app folder/urls.py/name)' %}
	```
	
### The Child Template
* A child template must have an `{% extends %}` tag on the first line to tell Django which parent template to inherit from.
* In a child template, we only need to include content that's unique to that page.
* To modify an element common to many pages, you only need to modify the element in the parent template.
* In a large project, it's common to have one parent template called base.html for the entire site and parent templates for each major section of the site. All the section templates inherit from base.html, and each page in the site inherits from a section template.  
### Python in Pages
* Python uses indentation to indicate which lines of a for statement are part of a loop.
* In a template, every for loop needs an explicit `{% endfor %} `tag indicating where the end of the loop occurs.
* Use the `{% empty %}` to tell Django what to do the if statement is false, which is equivalent to 'else'.
