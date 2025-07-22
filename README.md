perun-bird2
=========

Installs BIRD2 with custom configuration file

Requirements
------------

Debian 12 or later.

Role Variables
--------------

bird2_configuration_file: Path to the configuration file, which will be installed to /etc/bird/bird.conf

Dependencies
------------

None.

Example Playbook
----------------

- hosts: servers
  roles:
     - cesnet.bird2
  vars:
    bird2_configuration_file: "{{ inventory_hostname}}/bird/bird.conf"
