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

There's also an aegir-remote-host role, which does most of [this](http://community.aegirproject.org/node/30/) for remote apache/mysql servers for Aegir.

TODO / What this playbook doesn't do yet
----------------------------------------

* Set hostname (not sure if this is wise)
* Automatically deploy platforms
* Install specific PHP version?

What this does not do
---------------------

* Create valid credentials for the nagios frontend
