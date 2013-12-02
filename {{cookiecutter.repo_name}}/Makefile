app:
	cd django/{{cookiecutter.repo_name}}/ && cookiecutter https://github.com/rpedigoni/cookiecutter-django-app

test:
	coverage run --branch --source=django/{{cookiecutter.repo_name}}  django/{{cookiecutter.repo_name}}/./manage.py test django/{{cookiecutter.repo_name}}/ -v 2 --failfast --settings=settings.test
	coverage report --omit=django/{{cookiecutter.repo_name}}/*/migrations*,django/{{cookiecutter.repo_name}}/settings/*,django/{{cookiecutter.repo_name}}/urls.py,django/{{cookiecutter.repo_name}}/wsgi.py,django/{{cookiecutter.repo_name}}/manage.py,django/{{cookiecutter.repo_name}}/*/tests/*,django/{{cookiecutter.repo_name}}/__init__.py

html:
	coverage html --omit=django/{{cookiecutter.repo_name}}/*/migrations*,django/{{cookiecutter.repo_name}}/settings/*,django/{{cookiecutter.repo_name}}/urls.py,django/{{cookiecutter.repo_name}}/wsgi.py,django/{{cookiecutter.repo_name}}/manage.py,django/{{cookiecutter.repo_name}}/*/tests/*,django/{{cookiecutter.repo_name}}/__init__.py
	open htmlcov/index.html

doc:
	$(MAKE) -C docs/ html
	open docs/build/html/index.html

deploy:
	fab -f django/fabfile.py deploy

clean:
	rm -f .coverage
	rm -rf htmlcov/
	rm -rf docs/build/
