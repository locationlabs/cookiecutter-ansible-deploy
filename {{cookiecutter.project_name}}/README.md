# {{ cookiecutter.project_name }}

{{ cookiecutter.short_desc }}

## Required Setup

1. Create/activate a virtualenv for the project:

        mkvirtualenv {{ cookiecutter.project_name }} -r requirements.txt

2. Install shared roles required by the ansible deploy:

        ansible-galaxy install -r requirements.yml -p shared-roles --force

3. Add the following to your `~/.ssh/config`

        Host *.vagrant
         StrictHostKeyChecking no
         UserKnownHostsFile /dev/null

## Vagrant Deploy

    vagrant up
    ansible-playbook {{ cookiecutter.project_name }}.yml

## Deploy {{ cookiecutter.project_name }}

_Real deploy instructions go here_

    ansible-playbook -i inventory/<environment> {{ cookiecutter.project_name }}.yml
