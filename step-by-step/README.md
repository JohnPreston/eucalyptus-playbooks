Deploy Eucalyptus Cloud step-by-step
=====================================

Requirements
-------------

This playbook requires to have these roles setup from Ansible-Galaxy:

- JohnPreston.eucalyptus-network

- JohnPreston.eucalyptus-setup

- JohnPreston.eucalyptus-initialize

- JohnPreston.eucalyptus-register

- JohnPreston.eucalyptus-start

- JohnPreston.eucalyptus-configure

To set them all up, run 

```

ansible-galaxy install -r requirements.conf

```

How to use
----------

Each role has its own variables. You can use variables directly in the playbook or via vars_files.
To see each roles requirements and documentation, visit their ref. wab pages.

The most important is to create and configure your hosts file according to the different templates you will find in the inventory folder.

Run the playbook
----------------

```

ansible-playbook -i hosts/<hosts_file> site.yml

```

