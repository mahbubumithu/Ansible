Ansible is an open-source configuration management and provisioning tool, similar to Chef, Puppet or Salt.

It uses SSH to connect to servers and run the configured tasks. Ansible lets you control and configure nodes from a single machine.

Funded in 2013

Red Hat bought it in  2015.

## Why Ansible ?
- No agent
- Idempotent
- Declarative Not Procedural
- Tiny Learning Curve


## Ansible Use Cases:
- Provisioning
- Configuration Management
- App Deployment
- Continous Delivery
- Security & Compliance
- Orchestration



For Linux - SSH
For Windows - WinRM


## Inventory

The Inventory is a description of the nodes that can be accessed by Ansible.

By default the inventory is described by a configuration file, whose deafult location is in /etc/ansible/hosts

The configuration file lists either the IP address or hostname of each node that is accessible by Ansible.

The inventory file can be in one of many formats such as yaml, INI etc.



