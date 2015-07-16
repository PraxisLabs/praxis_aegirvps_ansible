Usage
-----

Before using:

1. Install ansible
2. Set up VMs like in test.hosts
3. Add public SSH keys to client the VMs' root user's authorized\_keys file (/root/.ssh/authorized\_keys)

You can now test the playbook on the server VM:

    ansible-playbook -s server.yml -i test.hosts -u root

Notes
-----

This playbook installs Aegir on clients using the debian package. By default, this will install using the hostname as the frontend url. This is just fine for us but might be a problem depending on your use case.

TODO / What this playbook doesn't do yet
----------------------------------------

* Set hostname (not sure if this is wise)
* Stop hosting\_queued
* Install Skynet
* Automatically deploy platforms
* Install and configure nagios (see nagios branch)
* Install specific PHP version?

What this does not do
---------------------

* Create valid credentials for the nagios frontend
