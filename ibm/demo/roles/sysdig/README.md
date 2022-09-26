sysdig
=========

To deploy a SysDig Agent on an Ubuntu VSI.

Requirements
------------

A SysDig ingestion endoint is required for this agent to operate properly. Network access to this endpoint is required.

Role Variables
--------------

**Defaults**

| variable        | Description                              | Example                   |
| --------------- | ---------------------------------------- | ------------------------- |
| sysdig_key      | Access key for the Sysdig Server         | "dfsdfsdfsdfsdf345j34o5n" |
| sysdig_port     | Port the Sysdig Server is listening on   | "6443"                    |
| sysdig_endpoint | Location of the Sysdig Server            | "ingest.private.us-south.monitoring.cloud.ibm.com"|
| sysdig_tags     | Agent tags                               | "web","prod"              |


Dependencies
------------

Nil

Example Playbook
----------------
```
  - hosts: localhost
    collections:
      - ibm.demo
    roles:
      - sysdig
```
License
-------

BSD

Author Information
------------------

IBM Cloud