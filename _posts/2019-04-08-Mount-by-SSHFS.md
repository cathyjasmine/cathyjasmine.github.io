---
title: Mount by SSHFS
date: 2019-04-07 20:46:22
tags: [ssh, remote mount]
categories: ubuntu
---

 SSHFS (SSH Filesystem) is a filesystem client to mount and interact with files located on a remote server or workstation over a normal ssh connection. It's safer and more convenient than *nfs*. And it's helpful especially when we are facing multiple servers and large dataset.

### Install

`sudo apt-get install sshfs`

### Mount remote filesystem

```
$ mkdir ~/remoteshared
$ sshfs <user>@<host>:/remotepath ~/remoteshared
```

### Uninstall

`umount ~/remoteshared`



### Tips

1. **read: Connection reset by peer**

   ```
   xxx@xxx:~$ sudo sshfs yanhd@172.23.65.122:/home/yanhd ./122
   read: Connection reset by peer
   xxx@xxx:~$
   ```

   Use the ssh port `-p <portnumber>`.  Check whether the `ssh` works.  If ssh works, sshfs will work. 