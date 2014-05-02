# Deploy Django with Ansible

An Opinionated [Ansible](http://ansible.com) deploy script for Django, Postgres, Nginx and Gunicorn I use to deploy some of my django apps.

ATTENTION: This is still a work in progress! The script does not do a full deploy, yet. But it will soon ;)

The configuration is a mix of solutions from different sources that work best for me.

Here are the articles I used to develop this deploy script:

* http://michal.karzynski.pl/blog/2013/06/09/django-nginx-gunicorn-virtualenv-supervisor/
* https://github.com/makaimc/sf-django
* https://www.digitalocean.com/community/articles/how-to-install-and-configure-django-with-postgres-nginx-and-gunicorn
* http://www.stavros.io/posts/example-provisioning-and-deployment-ansible/

# Getting Started

* Install Vagrant to test and tweak the script locally (https://www.vagrantup.com/downloads)
* Clone repo
* Install Ansible (Recommended: Via pip. Create a virtualev and run pip install -r requirements.txt within this repo's root dir)
* run source venv/bin/activate
* run vagrant up

# TODO
* Finish the script
* Add documentation

# License
MIT licensed.
