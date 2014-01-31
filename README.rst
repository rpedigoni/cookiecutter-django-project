cookiecutter-django-project
===========================

This is a simple Django cookiecutter based on the skeleton I've been using for years. It eases TDD with Django :)


Requirements
------------

You'll need two things to start:

    * ``virtualenvwrapper`` or just ``virtualenv`` if you prefer
    * ``cookiecutter``



Quickstart
----------

Run the command below and answer the questions: ::

    cookiecutter https://github.com/rpedigoni/cookiecutter-django-project.git


Create a ``virtualenv``: ::

    mkvirtualenv yourproject


And install the project dependencies: ::

    pip install -r django/requirements/development.txt


You're ready to go: ::

    make test


A more detailed guide will be available on your project's ``README.rst`` file... or `here`_.

.. _`here`: https://github.com/rpedigoni/cookiecutter-django-project/blob/master/%7B%7Bcookiecutter.repo_name%7D%7D/README.rst


Creating Django apps
--------------------

There's a helper on ``Makefile`` to create Django apps using ``cookiecutter-django-app`` template: ::

    make app


Other helpers
-------------

    * ``make test html``: opens the default web browser to check coverage details
    * ``make doc``: renders restructuredText documentation to HTML (edit them on ``docs/``)
    * ``make clean``: deletes coverage report and generated HTML docs
