Role Name
=========

To deploy a LogDNA Agent on an Ubuntu VSI.

Requirements
------------

A LogDNA ingestion endoint is required for this agent to operate properly. Network access to this endpoint is required.

Role Variables
--------------

**Defaults**

| variable        | Description                                         | Example          |
| --------------- | --------------------------------------------------- | ---------------- |
| logdna_install  | Boolean to determine whether to install the agent   | True             |
| logdna_dirs     | List of directories to manage.                      | ["/var/log"]     |
| logdna_exclude  | List of directories to exclude                      | ["/var/log/nginx/error.log"]|
| logdna_hostname | Over-ride of the Agent Hostname                     | ["demo.ibm.com"]  |
| logdna_tags     | List of Tags to add to the Agent                    | ["web"]|
| logdna_key      | LogDNA Key                                          |  "jb34kl5j34bb34j23"  |
| logdna_apihost  | LogDNA API Host                                     |  "api.us-south.logging.cloud.ibm.com "  |
| logdna_loghost  | LogDNA Key                                          |  "logs.private.us-south.logging.cloud.ibm.com"  |




| Role            | Description                                         | Operating Systems|
| --------------- | --------------------------------------------------- | ---------------- |
| logdna          | Role to deploy a LogDNA Agent on a VSI in IBM Cloud | Ubuntu 18.04 +   |
| sysdig          | Role to deploy a Sysdig Agent on a VSI in IBM Cloud | Ubuntu 18.04 +   |
| demo            | Role to deploy a Demo Application in IBM Cloud      | Ubuntu 18.04 +   |


Dependencies
------------

Nil

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

IBM Cloud
