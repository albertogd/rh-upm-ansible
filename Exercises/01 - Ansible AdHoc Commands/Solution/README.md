* Print "It is working" message on localhost

```
$ ansible localhost -c local -m debug -a 'msg="It is working"'
```

* Print instance settings on localhost
  
```
$ ansible localhost -c local -m setup
```  
    
* Create a new user "yourname" on localhost

```
ansible localhost -c local -m user -a "name=yourname" -b
```

* Include the new user "yourname" on **mail** group on localhost

```
$ ansible localhost -c local -m user -a "name=yourname groups=mail" -b
```

* Copy file **/etc/protocols** on localhost using and setting permissions 440 and owner root in **/tmp/<yourname>**

```
$ ansible localhost -c local -m copy -a "src=/etc/protocols dest=/tmp/yourname owner=root mode=0440" -b
```