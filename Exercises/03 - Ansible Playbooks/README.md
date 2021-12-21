# Ansible Playbooks

Playbooks record and execute Ansible’s configuration, deployment, and orchestration functions. They can describe a policy you want your remote systems to enforce, or a set of steps in a general IT process.

If Ansible modules are the tools in your workshop, playbooks are your instruction manuals, and your inventory of hosts are your raw material.

At a basic level, playbooks can be used to manage configurations of and deployments to remote machines. At a more advanced level, they can sequence multi-tier rollouts involving rolling updates, and can delegate actions to other hosts, interacting with monitoring servers and load balancers along the way.

Playbooks are designed to be human-readable and are developed in a basic text language. There are multiple ways to organize playbooks and the files they include, and we’ll offer up some suggestions on that and making the most out of Ansible.

## Steps 

-   Use the inventory created in Lab **02 - Ansible Inventory**
-   Create a playbook named backend_config.yml with the following options:
    -   The play must be executed on **frontends** hosts
    -   Print facts
    -   Create a new user "yourname"
    -   Install package "httpd"
    -   Enable and start "httpd" service on group 

---
**NOTE**

If you receive an error "Invalid callback for stdout specified: yaml", install the collection community.general:

$ ansible-galaxy collection install community.general
---

Before running your playbook, run the ansible-playbook --syntax-check  command to verify that its syntax is correct.

Run the playbook and verify results via curl http://node1

## Useful Links

For more information, please visit:

-   https://docs.ansible.com/ansible/latest/user_guide/playbooks.html
-   https://docs.ansible.com/ansible/latest/modules/modules_by_category.html
