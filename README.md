[![Build Status](https://img.shields.io/travis/ptavares/ansible-role-terragrunt/master.svg?style=flat-square)](https://travis-ci.org/ptavares/ansible-role-terragrunt)
[![Ansible Role](https://img.shields.io/ansible/role/29419.svg)](https://galaxy.ansible.com/ptavares/ansible-role-terragrunt)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](https://github.com/ptavares/ansible-role-terragrunt/blob/master/LICENSE)

ansible-role-terragrunt
=========

Ansible role for installating terragrunt executable

Requirements
------------

Only test with ansible 2.5 min version

Role Variables
--------------
Available variables are listed below, along with default values (see [defaults/main.yml](https://github.com/ptavares/ansible-role-terragrunt/blob/master/defaults/main.yml)):

### Terragrunt version 

```yaml
# By default, module will download last version
# To specify a version, use this below param
terragrunt_install_version: vX.X.X
```
### Download information

```yaml
# Directory where executable will be downloaded before installation
terragrunt_download_location: /tmp/
# Url to terragrunt binarie
terragrunt_url: "https://github.com/gruntwork-io/terragrunt/releases/download/{{ terragrunt_install_version }}/terragrunt_linux_amd64"
# Downloaded file name 
terragrunt_downloaded_file_name: terragrunt_linux_amd64
```

### Installation information

```yaml
# Path where to install terraform
terragrunt_execution_path: /usr/local/bin
# Execution file name for terraform
terragrunt_execution_file_name: terragrunt
```

Dependencies
------------

No dependencie

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: ptavares.ansible_role_terragrunt
```
Inside *`vars/main.yml`*:
- Copy content of [defaults/main.yml](https://github.com/ptavares/ansible-role-terragrunt/blob/master/defaults/main.yml) in your playbook's vars file if needed.
- Customize it as you like (filling role's variables)

License
-------

MIT
