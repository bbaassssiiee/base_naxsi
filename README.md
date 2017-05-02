-----------
base_naxsi is an experiment with ansible-container.
Naxsi is an application firewall for NGinx.

Requirements
------------

RHEL-like, rpm-build, gcc.


Role Variables
--------------
- nginx\_main_version: 1.12.0
- nginx\_release: 1 # the number after the dash (-)
- nginx\_replace: 3 # increment the nginx_release to allow an update with naxsi



Dependencies
------------

none

Example Usage
----------------


\#!/usr/bin/env ansible-playbook

\- name: example\ playbook

  hosts: all

  become: yes

  roles:

    - { role: bbaassssiiee.base_naxsi, tags: 'naxsi' }

Debug under ansible-container
-----------------------------
rm -rf ansible

ansible-container init

ansible-container --debug install bbaassssiiee.base_naxsi

ansible-container --debug build


License
-------

MIT

Author Information
------------------

Bas Meijer
@bbaassssiiee
