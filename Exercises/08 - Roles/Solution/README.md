# Ansible Roles

## Create a custom role named "mariadb" which has to implement the following tasks


```
$ ansible-galaxy init roles/mariadb
```

## Install the collections

- name: community.general
- name: community.mysql

```
$ ansible-galaxy collection install community.general
$ ansible-galaxy collection install community.mysql
```

## Run playbook


```
$ ansible-playbook -i inventory deploy_mariadb.yml
```

##   Test Database


```
$ ssh node2
$ sudo -i
$ mysql -u root
MariaDB [(none)]> $ show databases;
MariaDB [(none)]> $ SELECT Host,User FROM mysql.user;
```