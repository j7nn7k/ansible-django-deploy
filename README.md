# Deploy Django with Ansible

An opinionated [Ansible](http://ansible.com) deploy script for Ubuntu, Django, Postgres, Nginx and Gunicorn I use to deploy some of my django apps.

The configuration is a mix of solutions from different sources that work best for me.

Here are the articles I used to develop this deploy script:

* http://michal.karzynski.pl/blog/2013/06/09/django-nginx-gunicorn-virtualenv-supervisor/
* https://github.com/makaimc/sf-django
* https://www.digitalocean.com/community/articles/how-to-install-and-configure-django-with-postgres-nginx-and-gunicorn
* http://www.stavros.io/posts/example-provisioning-and-deployment-ansible/

# Getting Started

* Install Vagrant (https://www.vagrantup.com/downloads) and VirtualBox (https://www.virtualbox.org/)
* Clone/download this repo
* Install Ansible (Recommended: Via pip. To do that create a virtualev and run `pip install -r requirements.txt` within this repo's root dir)
* Add an inventory file in the repo's root dir called `hosts`. To test with vagrant paste the following content into the file: 


	[vagrant]
	default ansible_ssh_host=127.0.0.1 ansible_ssh_port=2222


* Add a deploy ssh key from your repo to let the app pull your code. Add a file called `deploy_key` to the directory `/roles/app/files/`
* tweak the `/group_vars/all.yml` file to comply with your app's setup
* Acivate your virtualenv (run `source venv/bin/activate`)
* From within this repo's root dir run `vagrant up`

## Celery (optional)
I you want to use celery set `install_celery: yes` in `group_vars/all.yml`

# TODO
* Add more documentation

# License
MIT licensed.
