Deploy Eucalyptus Cloud w/ RiakCS backend
=========================================

Requirements
-------------

** Ansible Galaxy - Roles **

This playbook requires to have these roles setup from Ansible-Galaxy:

- [JohnPreston.eucalyptus-network](https://github.com/JohnPreston/eucalyptus-network)

- [JohnPreston.eucalyptus-setup](https://github.com/JohnPreston/eucalyptus-network)

- [JohnPreston.eucalyptus-initialize](https://github.com/JohnPreston/eucalyptus-network)

- [JohnPreston.eucalyptus-register](https://github.com/JohnPreston/eucalyptus-network)

- [JohnPreston.eucalyptus-start](https://github.com/JohnPreston/eucalyptus-network)

- [JohnPreston.eucalyptus-configure](https://github.com/JohnPreston/eucalyptus-network)

To set them all up, run

```

ansible-galaxy install -r requirements.conf

```

** Hosts **

You will find some hosts examples inside the inventory folder. Treat them as templates or edit them to fit your environment.

| group_name | Description | mandatory variable | Note
|--- |--- |--- |---
| clc | Eucalyptus Cloud Controller | Must have a single host
| walrus | Eucalyptus Walrus | walrus_name | Must have a single host. The host is not mandatory
| ufs | Eucalyptus User Facing Services | ufs_name | Multi-Hosts supported. ufs_name must be unique
| cc | Eucalyptus Cluster Controller | cc_name | name must be unique
| sc | Eucalyptus Storage Controller | sc_name | name must be unique
| nc | Eucalyptus Node Controller | none | none


![Hosts file explanation](/playbook-demo.png?raw=true "Host deployment")


* Warning * in case you are going to use VLANs, you have to specify the vlan_ip you want to use, in CIDR notation.


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

