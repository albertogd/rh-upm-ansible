# Ansible AdHoc Commands

AdHoc command allows execute a single Ansible task in a programmatic and simple way. This lesson dives in this Ansible feature.

An ad hoc command looks like this:

```
$ ansible [pattern] -m [module] -a "[module options]"
```

## Examples

### Managing services
Ensure a service is started on all webservers:

```
$ ansible webservers -m ansible.builtin.service -a "name=httpd state=started"
```


### Managing files
The ansible.builtin.file module allows changing ownership and permissions on files.

```
$ ansible webservers -m ansible.builtin.file -a "dest=/srv/foo/b.txt mode=600 owner=mdehaan group=mdehaan"
```

## Exercise 

- Execute different Ansible Ad-Hoc Commands in order to achieve the following objectives:
    * Print "It is working" message on localhost
    * Print instance settings on localhost
    * Create a new user "yourname" on localhost using become (root)
    * Include the new user "yourname" on **wheel** group on localhost using become (root)
    * Copy sudo file **/etc/passwd** on localhost using become "yourname" and setting permissions 440 and owner root in **/tmp/newfile**

## Useful Links

For more information, please visit:

-  https://docs.ansible.com/ansible/latest/user_guide/intro_adhoc.html
