==============================
Copier Python package template
==============================

A copier template to get started with a GitHub-based python package / CLI application. 

What's inside?
--------------
* A very minimal python package with a CLI
* CLI skeleton using Click 
* CI/CD using GitHub-Actions
* Dependabot updates for dependencies and GitHub-Actions
* Pre-commit updates via GitHub-Action
* Testing using tox, pytest, coverage/pytest-cov
* Pre-commit configuration
* Linting, code formatting using flake8, black and isort
* .editorconfig 
* pyproject.toml + setup.cfg + setup.py
* Requirements subfolder with dev.txt, test.txt and prod.txt

How to use
----------
There are several steps necessary to get started with this template:

Initial copy:
=============
The following instructions are only necessary to execute once, when you start with your new package.

* Install copier (Instructions can be found in their documentation_)
* Create a destination project directory
* In case you intend to update the template in the future: The destination needs to be a git repository.
* ``copier copy gh:hfrSchmidt/copier-template-py-package <destination directory>``
* Answer the questions.
* Create a python3 virtual environment. For example: ``python3 -m venv .venv``.
* Activate the virtual environment: ``source .venv/bin/activate``
* Install the dependencies you need. For example the development dependencies: ``python3 -m pip install -r requirements/dev.txt``
* Install pre-commit hooks (if you want to use pre-commit): ``pre-commit install``
* Start coding...

If you want to automatically create PRs to update the pre-commit hooks' revisions, you need to additionally create a 
"fine-grained personal access token" (FPAT_) for your repository. This is especially important for being able to trigger other CI actions
on automatically created PRs, so you can be confident that an update of a dependency / pre-commit hook does not break your CI.
The FPAT needs to be scoped to your target repository and needs repository permissions to read metadata and read + write access 
to content as well as pull requests.
After you have generated the FPAT add it to the repository as a secret called "FPAT".
There are other means of achieving this available from here_

Update:
=======
When you want to update your package with the newest version of the template use the following:

* ``copier update``

You will be asked all the questions from the initial generation again. In case you want to skip the questions and use your previous answers:

* ``copier -f update``

.. _documentation: https://copier.readthedocs.io/en/stable/
.. _FPAT: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token
.. _here: https://github.com/peter-evans/create-pull-request/blob/main/docs/concepts-guidelines.md#triggering-further-workflow-runs