eucalyptus-playbooks
====================

Ansible playbooks to deploy Eucalyptus using eucalyptus roles

Step-By-Step
------------

This playbook will allow the users to work on Eucalyptus deployments faster, focusing on the needs to change variables directly in the playbook file for each step of Eucalyptus deployment. This aim to give more possibilities in the deployment of Eucalyptus in order to test it, for QA.

RiakCS integration
------------------

This playbook focused to integrate RiakCS as Object Storage backend. This allows to have a scalable, high-available storage sytem for your images and buckets. The more nodes you have in the ring, the best are your performances and reliability.
This playbook also has example files for a multi-cluster deployment. Consider multi-cluster if you need high availability on different sites (even just in different rooms of your DataCenter).

Requirements
------------

Please, read the documentation about Eucalyptus : https://eucalyptus.com/docs
Documentation about the roles can be found under the github reporsitories
