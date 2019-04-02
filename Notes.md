# start project
>> django-admin startproject mysite

# Run on custom port
>> python manage.py runserver 8080

# startapp and startproject is different - project is web of multiple apps etc.
# start app
>> python manage.py startapp polls

# You should always use include() when you include other URL patterns. admin.site.urls is the only exception to this.
urlpatterns = [
    path('polls/', include('polls.urls')),
    path('admin/', admin.site.urls),
]

# DATABASE
ENGINE – Either 'django.db.backends.sqlite3', 'django.db.backends.postgresql', 'django.db.backends.mysql', or 'django.db.backends.oracle'. Other backends are also available.

NAME – The name of your database. NAME should be the full absolute path ==> os.path.join(BASE_DIR, 'db.sqlite3')

# To setup database
>> python manage.py migrate

# to test open sqllite client
>> sqlite3 db.sqlite3
# and tun
>> .schema 
#will give all  tables created

The default applications are included for the common case, but not everybody needs them. If you don’t need any or all of them, feel free to comment-out or delete the appropriate line(s) from INSTALLED_APPS before running migrate. 

# Each field is represented by an instance of a Field class 
# – e.g:  CharField     for character fields and 
#         DateTimeField for datetimes. 
