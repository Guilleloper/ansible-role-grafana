# ANSIBLE ROLE GRAFANA

## Description
Ansible role for Grafana deployment.

(See Grafana repository: https://github.com/grafana/grafana)
<br/><br/>

## Prepare an Ansible environment for deploying the role
Steps to prepare an Ansible environment for deploying the role:
```
$ cd <deployment location>
$ view grafana.yml
~
---
- hosts: grafana
  become: True
  gather_facts: False
  roles:
    - grafana
...
~
$ mkdir roles
$ cd roles/
$ git clone https://github.com/Guilleloper/ansible-role-grafana
$ mv ansible-role-grafana/ grafana/
$ cd ..
```
<br/><br/>
## Deploy Grafana:
```
$ ansible-playbook grafana.yml --diff --check
$ ansible-playbook grafana.yml --diff
```
