# Ansible Inventory

Ansible works against multiple managed nodes or “hosts” in your infrastructure at the same time, using a list or group of lists known as inventory. Once your inventory is defined, you use patterns to select the hosts or groups you want Ansible to run against.

The default location for inventory is a file called /etc/ansible/hosts. You can specify a different inventory file at the command line using the -i <path> option

## Steps 

Create an Ansible inventory file named "inventory" with the following requisites:

-   A group named **webservers** with 2 subgroups **frontend** and **backends**
-   **node1** belongs to **frontends** group
-   **node2** and **node3** belongs to **backends** group
-   Define an ansible var **app_version** with the value **1.0** for **webservers** group 
-   Define an ansible var **http_port** with the value **80** for **frontends** group
-   Define an ansible var **db_port** with the value **3306** for **backends** group
-   Check inventory file structure is correct and graphs it
-   Print the var **http_port** for **frontends** group

## Useful Links

For more information, please visit:

-   https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html#intro-inventory
-   https://docs.ansible.com/ansible/latest/cli/ansible-inventory.html