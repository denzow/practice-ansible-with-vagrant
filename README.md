practice ansible with vagrant
==================================

### setup


#### add box

```
$ vagrant box add --name ol69 http://yum.oracle.com/boxes/oraclelinux/ol69/ol69.box
```

#### init vagrant

```
$ vagrant box add --name ol73 http://yum.oracle.com/boxes/oraclelinux/ol73/ol73.box
$ vagrant init ol73
$ vagrant up
```

#### test connect

```
$ vagrant ssh
```

### ansible check

```
$ ansible -i provisioning/inventory.ini all -m ping
127.0.0.1 | SUCCESS => {
    "changed": false,
    "ping": "pong"
}
```

