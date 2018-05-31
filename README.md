SDCOMMON
=========

Install and configures directory structure and required packages.

Requirements
------------

```
None
```

Role Variables
--------------

```
---
# vars file for common
data_dir: /data
apps_dir: /apps

# Libraries and utilities
apt_libraries_utilities:
- ntp
- lsof
- wget
- python-software-properties
- zip
- unzip
- build-essential

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
- hosts: test_servers
  become: yes
  gather_facts: yes
  roles:
    - role: common
    - role: sdjava
      tags: java
    - role: maven
      tags: maven
```

License
-------

Licensed under the Apache License V2.0. See the [LICENSE file](LICENSE) for details.

Author Information
------------------

Author: Shashi yebbare
