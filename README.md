# polls-app

To install the package, use pip :

python -m pip install --user django-polls/dist/django-polls-0.1.tar.gz
Update <your-django-project>/settings.py to point to the new module name:

INSTALLED_APPS = [
    "django_polls.apps.PollsConfig",
    ...,
]
Update <your-django-project>/urls.py to point to the new module name:

urlpatterns = [
    path("polls/", include("django_polls.urls")),
    ...,
]
Run below comamnd and see if it works:

python manage.py runserver