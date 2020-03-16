# Django Project

## Starting up

* Create a virtualenv and install requirements from `requirements.txt`.

* Create a PostgreSQL database (e.g. `mysite`).

* To set up the database connection, either edit `DATABASES` in  `settings.py`, or pass the appropriate environment variables (`PSQL_DB_NAME` etc.)

* Now run the databse migrations for the project. If the parameters are right, `python manage.py migrate` should work:

```
$ python manage.py migrate
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying admin.0003_logentry_add_action_flag_choices... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying auth.0009_alter_user_last_name_max_length... OK
  Applying auth.0010_alter_group_name_max_length... OK
  Applying auth.0011_update_proxy_permissions... OK
  Applying sessions.0001_initial... OK
```

* You can also create a user account by running `python manage.py createsuperuser`.

## Running the server

```
python manage.py runserver
```

By default, the server will run at http://127.0.0.1:8000/.
