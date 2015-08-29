# ansible exec over step-server

## provision

```
$ vagrant up
$ vagrant ssh worker
```

## make admin user

```
vagrant@worker:~$ sudo adduser aworker
vagrant@worker:~$ sudo usermod aworker -g admin
vagrant@worker:~$ logout
```

## test

### ping

```
$ ansible -i hosts worker -m ping
SSH password: 
worker | success >> {
      "changed": false, 
          "ping": "pong"
}
```

### playbook

```
$ ansible-playbook -i hosts test.yml 
SSH password: 

PLAY [all] ******************************************************************** 

GATHERING FACTS *************************************************************** 
ok: [worker]

TASK: [get hostname] ********************************************************** 
changed: [worker]

TASK: [print hostname] ******************************************************** 
ok: [worker] => {
      "msg": "worker"
}

PLAY RECAP ******************************************************************** 
worker                     : ok=3    changed=1    unreachable=0    failed=0   
```

