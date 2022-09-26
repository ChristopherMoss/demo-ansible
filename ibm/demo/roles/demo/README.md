demo
=========

To deploy a simple demo application on a VSI. The demo application will run on a python based uvicorn server.

Requirements
------------

Nil

Role Variables
--------------

**Defaults**

| variable        | Description                              | Example                   |
| --------------- | ---------------------------------------- | ------------------------- |
| demo_role      | Role of the server        | either "front or "back" |
| demo_lb_back     | Address of the application load balancer   | "1e238205-us-south.lb.appdomain.cloud" |

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
      - demo
```
License
-------

BSD

Author Information
------------------

IBM Cloud