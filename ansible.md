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


Playbook contains Plays
Plays contain tasks
Tasks call modules

Playbook Example:

---
- hosts: web
  remote_user root
  tasks:
    - name: ensure apache is at the latest version
      yum: name=httpd state=latest
    - name: ensure apache is running
      service: name=httpd state=started enabled=yes
...

Modules:
2000 modules provided by Ansible to automate every part of the environment.

Modules are like plugins.

There are lots of modules such as--
Service, file, copy, iptables etc.

Any Module can be used as --

ansible 127.0.0.1 -m service -a "name=httpd state=started"
ansible localhost -m ping


Ansible is agentless. So we do not need to install any software on the servers that are to be managed. It does require Python runtime on the servers are a SSH server on remote hosts.

Ansible supports both push and pull modes. So we can execute Ansible code from a central control machine to make changes on remote machines or the remote machines can pull configuration from a well defained source periodically.

Code for Ansible is written in YAML.

Ansible Architecture
- Control Node
- Managed Nodes
- Inventory
- Modules
- Tasks
- Playbooks





