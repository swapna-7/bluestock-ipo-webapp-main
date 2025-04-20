## Setting Up PostgreSQL Database

1. **Install PostgreSQL:**

   Make sure PostgreSQL is installed on your system. You can download it from the official [PostgreSQL website](https://www.postgresql.org/download/).

2. **Create a PostgreSQL Database and User:**

   Once PostgreSQL is installed, create a new database and a user for your Django application. You can do this using the PostgreSQL command-line interface (`psql`) or a graphical tool like pgAdmin.

   Open your terminal and run the following commands:


CREATE DATABASE bluestock;
CREATE USER swapna WITH PASSWORD '12345';
ALTER ROLE swapna SET client_encoding TO 'utf8';
ALTER ROLE swapna SET default_transaction_isolation TO 'read committed';
ALTER ROLE swapna SET timezone TO 'UTC';
GRANT ALL PRIVILEGES ON DATABASE bluestock TO daiyanalam;



Install PostgreSQL Adapter for Python

pip install psycopg2-binary



DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'ipo',
        'USER': 'swapna',
        'PASSWORD': '12345',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}

Apply Migrations:
-->python3 manage.py makemigrations

-->python3 manage.py migrate

-->python3 manage.py runserver

