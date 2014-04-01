
Ansible Examples
----------------

This repository contains examples and best practices for building Ansible Playbooks.

It is adapted from https://github.com/ansible/ansible-examples and is intended to be used with a Vagrant/Ansible/Tower demo found here:

https://github.com/dfederlein/vagrant-tower

This is changed in the following ways:

- user is no longer root, it is remote_user: vagrant with sudo: true and sudo_user: root.
- where possible, ansible default ipv4 variable has been changed to ansibe_eth1.ipv4.address to conform to Virtualbox's network scheme per the VagrantFile of the above demo.
- host files in the original playbooks were removed, instead using a host file with all applicable groups and hosts in the demo placed at /etc/ansible/hosts in the Tower host.
- Any broken links, outdated syntax or other errors of omission have been corrected. These all will run on the Tower demo.
- any roles that begin with "aws" are intended to be demonstrated within ec2/VPC for AWS, user is root, group names have been changed to tag_Name_(something) to reflect AWS nomenclature.