perun-bird2
=========

Installs BIRD2 with custom configuration file

Requirements
------------

Debian 12 or later.

Role Variables
--------------

bird2_configuration_file: Path to the configuration file, which will be installed to /etc/bird/bird.conf
bird2_monitor_script: Path to the monitor script, which controls BIRD by running birdc commands. If specified, the
bird-monitor.service will be enabled to run this script as user bird-monitor, group bird.

Dependencies
------------

None.

Example Playbook
----------------
```
- hosts: servers
  roles:
    - cesnet.bird2
  vars:
    bird2_configuration_file: "{{ inventory_hostname}}/bird/bird.conf"
    # bird2_monitor_script: bird2_monitor.py # optional
```