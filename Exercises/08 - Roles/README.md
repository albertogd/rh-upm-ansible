# Ansible Roles

## Roles
Roles let you automatically load related vars, files, tasks, handlers, and other Ansible artifacts based on a known file structure. After you group your content in roles, you can easily reuse them and share them with other users.

### Role directory Structure
An Ansible role has a defined directory structure with eight main standard directories. You must include at least one of these directories in each role.

### Using roles at play level:

```
- hosts: webservers
  roles:
    - common
    - webservers
```

## Exercise

- Use the inventory created in Exercise 2 (if you don't have it, you can copy from Solution)
-   Create a custom role named "mariadb" which has to implement the following tasks:
    -   Install mariadb-server and python3-PyMySQL packages
    -   Start and enable mysqld service
    -   Create a database defined in "mysql_database" (* "testroles01" by default)
    -   Include a tasks file named "create_mariadb_user.yml" located in tasks folder. It is necessary to import this task file as many times as the number of users defined in an array variable named "mysql_users" (* At least "test01" by default) using a loop. Rename the loop var using loop controls. Regarding this tasks file, it has to perform the following tasks:
        -   Create a database named after the user
        -   Add user with password "password01" and full privileges to both the database named after said user and to "testroles01" database, from `<myinstance_ip>`
-   Create a playbook named "deploy_mariadb.yml". This playbook should install and configure MariaDB in backends server with the following users: test01, test02, test03.

## Useful Links

For more information, please visit:

-   https://docs.ansible.com/ansible/latest/user_guide/playbooks.html
-   https://docs.ansible.com/ansible/latest/modules/modules_by_category.html
-   https://docs.ansible.com/ansible/latest/user_guide/playbooks_intro.html
-   https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html
-   https://docs.ansible.com/ansible/latest/modules/import_tasks_module.html
-   https://galaxy.ansible.com
-   https://github.com/linux-system-roles/timesync
-   https://docs.ansible.com/ansible/latest/user_guide/playbooks_loops.html
