# Ansible Collection - IBM Demo

Roles for IBM Cloud Demo scenarios, not to be used for production. Produced as supporting material for showcasing IBM Cloud architectual patterns

## Roles

| Role            | Description                                         | Operating Systems|
| --------------- | --------------------------------------------------- | ---------------- |
| logdna          | Role to deploy a LogDNA Agent on a VSI in IBM Cloud | Ubuntu 18.04 +   |
| sysdig          | Role to deploy a Sysdig Agent on a VSI in IBM Cloud | Ubuntu 18.04 +   |
| demo            | Role to deploy a Demo Application in IBM Cloud      | Ubuntu 18.04 +   |

## Using this collection

These roles are designed to be installed in a high  curated manner from User Data in a newly deploy VSI. The following will deploy on Ubuntu Only. Please note, Python3 must first be installed before running this collection.

Extract from a VSI *User Data*.

```bash

  - python3 -m pip install ansible
  - ansible-galaxy collection install [THIS URL]#/ibm/demo
  - cd /root; ansible-playbook --extra-vars @ansible_variables.yml ansible_playbook.yml

```

Each Role will have a prescribed list of variables which are required to be generated prior to running.