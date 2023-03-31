=============================
Copier Python CLI template
=============================

A copier template to get started with a GitHub-based python CLI application. 

What's inside?
--------
* A very minimal python package with a CLI
* CLI skeleton using Click 
* CI/CD using GitHub-Actions
* Testing using tox, pytest, coverage/pytest-cov
* Pre-commit configuration
* Linting, code formatting using flake8, black and isort
* .editorconfig 
* pyproject.toml + setup.cfg + setup.py
* Requirements subfolder with dev.txt, test.txt and prod.txt

How to use
--------
There are several steps necessary to get started with this template:
* Install copier (Instructions can be found in their documentation_)
* Create a destination project directory
* In case you intend to update the template in the future: The destination needs to be a git repository.
* `copier copy gh:hfrSchmidt/copier-template-py-package <destination directory>`
* Answer the questions.
* Create a python3 virtual environment. For example: `python3 -m venv .venv`.
* Activate the virtual environment: `source .venv/bin/activate`
* Install the dependencies you need. For example the development dependencies: `python3 -m pip install -r requirements/dev.txt`
* Install pre-commit hooks (if you want to use pre-commit): `pre-commit install`
* Start coding...
* When you want to update the template to the newest version: `copier update`

.. _documentation: https://copier.readthedocs.io/en/stable/

