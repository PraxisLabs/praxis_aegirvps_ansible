Usage
-----

This is a playbook forked from Praxis AegirVPS to use in the creation of AMIs through Packer.

You'll need to install Ansible before you can use this.

Testing
-------

To test this in Vagrant, you'll need to specify the SQL user, host and password. In prod it would be something like this:
ansible-playbook -s server.yml --extra-vars "aegir_mysql_host=[amazon RDS DB] aegir_mysql_user=[amazon RDS user] aegir_mysql_password=[amazon RDS password]"

Deployment
----------

We'll use packer.yml to make images with as much stuff installed as possible. We'll use full.yml in prod.



Developped by Praxis Labs for Advisor Websites.
