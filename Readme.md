A simple todo app Django Restframework with React frontend.
React frontend only lists the current todos.
API end points are api/ and api/id

# Django RestAPI Framework 
![DS36-React-frontend (3)](https://user-images.githubusercontent.com/43504027/142686963-0ecd2115-4691-441c-a8f4-2adf2d3790c2.png)
![DS36-React-frontend (2)](https://user-images.githubusercontent.com/43504027/142686962-770fe0c6-5e55-4619-9ca7-09106370a64f.png)
# React App
![DS36-React-frontend (1)](https://user-images.githubusercontent.com/43504027/142686961-ffdf3ac5-3464-4b53-950d-3aa216e4ccff.png)

# How to Run:
1. clone the repo,
2. two folders: backend contains django appi frontend contains very basic react app
3. cd to backend, activate environment, install the apps in requirements.txt and run the app.  You can access Browsable API http://127.0.0.1:8000/api url. 
4. cd to frontend, install react apps the npm start in local host. You will see a list of ToDos that you have created via using Browsable API above.
5. This is a simple proj. and the key is to understand how backend and frontend talks to each other. See below for details.
6.Happy coding!!!


# Smth to note:
If using django for backend, you need to do the following 6 things:
1.ensure you are in the virtualenv, then 'pip install django-cors-headers'
2. add the following in your INSTALLED-APPS section of the settings.py: 'corsheaders',
3. add the following in the MIDDLEWARE section of the settings.py: 'corsheaders.middleware.CorsMiddleware',
4. 'django.middleware.common.CommonMiddleware',
5. add either of the following at the bottom of the settings.py:
    CORS_ORIGIN_ALLOW_ALL = True or

    CORS_ORIGIN_WHITELIST = [
    'http://localhost:3000',
    'http://127.0.0.1:3000'
  ]
  
 6. When using CORS_ORIGIN_WHITELIST, use the URL of the front end app where the GET Or POST request is coming from.
Another gotcha is ensuring the URL pointing to django ends with a trailing slash.
