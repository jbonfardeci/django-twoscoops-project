# How to setup a Django project in a virtual environment:

# 1. Install virtualenv:

pip install virtualenv

# 2. Usage to set up a new virtual environment:

virtualenv ~/.envs/<project_name>

# or specify version of Python to use in virtual environment

virtualenv -p /usr/bin/python2.7 ~/.envs/<project_name>

# 3. To begin using the virtual environment, it needs to be activated:

source ~/.envs/<project_name>/bin/activate

#	If you are done working in the virtual environment for the moment, you can deactivate it:

deactivate

#	To delete a virtual environment, just delete its folder:

rm -rf venv

# 4. install Two Scoops Django template

django-admin.py startproject --template=https://github.com/jbonfardeci/django-twoscoops-project/zipball/master --extension=py,rst,html <my_site_name>

# 5. Install requirements for local env: open <my_site_name>/requirements.txt, change "production.txt" to "local.txt"
#	then run:

pip install -r requirements
