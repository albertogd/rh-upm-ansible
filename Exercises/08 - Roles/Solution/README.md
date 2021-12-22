# Ansible Roles

## Create a custom role named "mariadb" which has to implement the following tasks


```
$ ansible-galaxy init roles/mariadb
```

## Run playbook


```
$ ansible-playbook deploy_mariadb.yml
```

##   Test Database


```
$ ssh node2
$ sudo -i
$ mysql -u root -p
MariaDB [(none)]> $ show databases;
MariaDB [(none)]> $ show grants for 'test01'@'xxx';
MariaDB [(none)]> $ show grants for 'test02'@'xxx';
MariaDB [(none)]> $ show grants for 'test03'@'xxx';
```