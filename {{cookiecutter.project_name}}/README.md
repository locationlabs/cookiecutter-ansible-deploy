# {{ cookiecutter.project_name }}

{{ cookiecutter.short_desc }}

## Required Setup

1. Create/activate a virtualenv for the project:

        mkvirtualenv {{ cookiecutter.project_name }}

1. Install the python requirements (ansible):

        pip install -r requirements.txt

1. Install shared roles required by the ansible deploy:

        ansible-galaxy install -r requirements.yml -p shared-roles --force

## Vagrant Deploy

    vagrant up
    ansible-playbook -i inventory/vagrant {{ cookiecutter.project_name }}.yml

## Deploy {{ cookiecutter.project_name }}

_Real deploy instructions go here_
