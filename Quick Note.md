# QUICK NOTE
* Creating a new app
* defining models: equivalent to create table in SQL
* activating models
	* add the app into settings.py
	* modify the database  
`python manage.py make migrations`  
`python manage.py migrate`

## Making Pages
### Three stages
* Defining URLs  
* Writing Views  
* Writing templates

### URL
Users request pages by entering URLs into a browser and clicking links.  

**First**
Decide what URLs are needed in the project.  
**Base URL**  
	# project folder    
	# apps folder  

1. Modify the urls.py in the project folder  
In this urls.py file, which represents the projects as a whole, which sets of URLs from the apps in the project.  
urlpatterns  
2. Create a new urls.py file in the app folder  
urlpattern
3. Writing a View  
In the app folder  index(request)  
4. Writing a Template  
index.html
5. /project folder/setting.py/  
```
TEMPLATES {  
'DIRS': [os.path.join(BASE_DIR, '')]  }
```