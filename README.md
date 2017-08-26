# ubuntu-python3-mssql
Ubuntu 16.04 with python 3.6 and MSSQL Client Drivers

## django setup
Usage for this was initially for django connecting to an ms sql server for its database.

Required python packages for django:
```
$ pip install django django-pyodbc-azure
```

Example settings:
```
DATABASES = {
    'default': {
         'ENGINE': 'sql_server.pyodbc',
         'NAME': '<db name>',
         'USER': '<db username>',
         'PASSWORD': '<db password>',
         'HOST': '<server ip or azure conn string>',
         'PORT': '<port>',
         'OPTIONS': {
             'driver': 'ODBC Driver 13 for SQL Server',
             'MARS_Connection': 'True',
         }
     }
}
```
