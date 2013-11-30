{{cookiecutter.repo_name}}
==========================

Installation
------------

Create a virtualenv (use ``virtualenvwrapper``): ::

    mkvirtualenv {{cookiecutter.repo_name}}


Install requirements via ``pip``: ::

    pip install django/requirements/development.txt


Create database tables: ::

    # on django/{{cookiecutter.repo_name}}
    ./manage.py syncdb --all --settings=settings.development


Run the project: ::

    # on django/{{cookiecutter.repo_name}}
    ./manage.py runserver --settings=settings.development


Tests
-----

To run the test suite, execute: ::

    make test


To show coverage details (in HTML), use: ::

    make test html
