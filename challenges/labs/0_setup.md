** List the cloud provider you are using (AWS, GCE, Azure, other) **
```
AWS
```

** List the Linux release you have chosen **
```
CentOS Linux release 7.2.1511 (Core) 
```


** Show that the disk space on each node is at least 30 GB **
```
[root@chale ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
devtmpfs                 7.3G     0  7.3G   0% /dev
tmpfs                    7.2G     0  7.2G   0% /dev/shm
tmpfs                    7.2G  8.3M  7.2G   1% /run
tmpfs                    7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvda1               497M  224M  274M  46% /boot
tmpfs                    1.5G     0  1.5G   0% /run/user/1000

[root@chalm ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
devtmpfs                 7.3G     0  7.3G   0% /dev
tmpfs                    7.2G     0  7.2G   0% /dev/shm
tmpfs                    7.2G  8.3M  7.2G   1% /run
tmpfs                    7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvda1               497M  224M  274M  46% /boot
tmpfs                    1.5G     0  1.5G   0% /run/user/1000

[root@chalw1 ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
devtmpfs                 7.3G     0  7.3G   0% /dev
tmpfs                    7.2G     0  7.2G   0% /dev/shm
tmpfs                    7.2G  8.3M  7.2G   1% /run
tmpfs                    7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvda1               497M  224M  274M  46% /boot
tmpfs                    1.5G     0  1.5G   0% /run/user/1000

[root@chalw2 ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
devtmpfs                 7.3G     0  7.3G   0% /dev
tmpfs                    7.2G     0  7.2G   0% /dev/shm
tmpfs                    7.2G  8.3M  7.2G   1% /run
tmpfs                    7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvda1               497M  224M  274M  46% /boot
tmpfs                    1.5G     0  1.5G   0% /run/user/1000

[root@chalw3 ~]# df -h
Filesystem               Size  Used Avail Use% Mounted on
/dev/mapper/centos-root   48G  1.9G   46G   4% /
devtmpfs                 7.3G     0  7.3G   0% /dev
tmpfs                    7.2G     0  7.2G   0% /dev/shm
tmpfs                    7.2G  8.3M  7.2G   1% /run
tmpfs                    7.2G     0  7.2G   0% /sys/fs/cgroup
/dev/xvda1               497M  224M  274M  46% /boot
tmpfs                    1.5G     0  1.5G   0% /run/user/1000

```

** List the command and output for yum repolist enabled **

```
[root@chale ~]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                             repo name                             status
base/7/x86_64                       CentOS-7 - Base                       9,591
extras/7/x86_64                     CentOS-7 - Extras                       227
updates/7/x86_64                    CentOS-7 - Updates                      741
repolist: 10,559
 
[root@chalm ~]#  yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                             repo name                             status
base/7/x86_64                       CentOS-7 - Base                       9,591
extras/7/x86_64                     CentOS-7 - Extras                       227
updates/7/x86_64                    CentOS-7 - Updates                      741
repolist: 10,559

[root@chalw1 ~]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                             repo name                             status
base/7/x86_64                       CentOS-7 - Base                       9,591
extras/7/x86_64                     CentOS-7 - Extras                       227
updates/7/x86_64                    CentOS-7 - Updates                      741
repolist: 10,559

[root@chalw2 ~]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                             repo name                             status
base/7/x86_64                       CentOS-7 - Base                       9,591
extras/7/x86_64                     CentOS-7 - Extras                       227
updates/7/x86_64                    CentOS-7 - Updates                      741
repolist: 10,559

[root@chalw3 ~]# yum repolist enabled
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: ftp.heanet.ie
 * extras: ftp.heanet.ie
 * updates: ftp.heanet.ie
repo id                             repo name                             status
base/7/x86_64                       CentOS-7 - Base                       9,591
extras/7/x86_64                     CentOS-7 - Extras                       227
updates/7/x86_64                    CentOS-7 - Updates                      741
repolist: 10,559

```
** List the /etc/passwd entries for ernest and siwicki in your setup file **
```
ernest:x:2000:2000::/home/ernest:/bin/bash
siwicki:x:3000:3000::/home/siwicki:/bin/bash
```
** List the /etc/group entries for usa and emea in your setup file **
```
usa:x:3001:ernest
emea:x:3002:siwicki
```

