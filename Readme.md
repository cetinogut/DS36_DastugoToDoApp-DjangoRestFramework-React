A simple todo app Django Restframework with React frontend.
React frontend only lists the current todos.
API end points are api/ and api/id

smth to note:
If using django for backend, you need to do the following 6 things:

ensure you are in the virtualenv, then 'pip install django-cors-headers'

add the following in your INSTALLED-APPS section of the settings.py: 'corsheaders',

add the following in the MIDDLEWARE section of the settings.py: 'corsheaders.middleware.CorsMiddleware',
'django.middleware.common.CommonMiddleware',

add either of the following at the bottom of the settings.py:
CORS_ORIGIN_ALLOW_ALL = True or

CORS_ORIGIN_WHITELIST = [
'http://localhost:3000',
'http://127.0.0.1:3000'
]
When using CORS_ORIGIN_WHITELIST, use the URL of the front end app where the GET Or POST request is coming from.

Another gotcha is ensuring the URL pointing to django ends with a trailing slash.