Ansible Role: common
=====================
Install and configures directory structure and required packages on RedHat/CentOS and Debian/Ubuntu

Requirements
------------
Requires the EPEL repository for RedHat/CentOS


Role Variables
--------------
Data and Apps diretory for all installations
```
data_dir: /data
apps_dir: /apps
```

Libraries and utilities for Debian/Ubuntu systems
```
apt_libraries_utilities:
- ntp
- lsof
- wget
- python-software-properties
- zip
- unzip
- build-essential
```
Libraries and utilities for RedHat/CentOS
```
yum_libraries_utilities:
- ntp
- lsof
- wget
- policycoreutils-python
- zip
- unzip
- vim
- dkms
- iptables-services
- kernel-devel
- kernel-tools
```

Dependencies
------------

```
None
```

Example Playbook
----------------

Use the following playbook:

```
- hosts: all
  become: yes
  gather_facts: yes
  roles:
    - role: common
```

License
-------

Licensed under the Apache License V2.0. See the [LICENSE file](LICENSE) for details.

Author Information
------------------

This role was created in 2014 by [Shashi Yebbare](https://www.skydevops.co.in/), author of [SkyDevops](https://www.skydevops.co.in/).
