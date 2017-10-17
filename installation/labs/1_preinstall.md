[centos@sebcm ~]$ sysctl vm.swappiness
vm.swappiness = 1

[centos@sebcm ~]$ mount
sysfs on /sys type sysfs (rw,nosuid,nodev,noexec,relatime)
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime)
devtmpfs on /dev type devtmpfs (rw,nosuid,size=7607712k,nr_inodes=1901928,mode=755)
securityfs on /sys/kernel/security type securityfs (rw,nosuid,nodev,noexec,relatime)
tmpfs on /dev/shm type tmpfs (rw,nosuid,nodev)
devpts on /dev/pts type devpts (rw,nosuid,noexec,relatime,gid=5,mode=620,ptmxmode=000)
tmpfs on /run type tmpfs (rw,nosuid,nodev,mode=755)
tmpfs on /sys/fs/cgroup type tmpfs (ro,nosuid,nodev,noexec,mode=755)
cgroup on /sys/fs/cgroup/systemd type cgroup (rw,nosuid,nodev,noexec,relatime,xattr,release_agent=/usr/lib/systemd/systemd-cgroups-agent,name=systemd)
pstore on /sys/fs/pstore type pstore (rw,nosuid,nodev,noexec,relatime)
cgroup on /sys/fs/cgroup/cpu,cpuacct type cgroup (rw,nosuid,nodev,noexec,relatime,cpuacct,cpu)
cgroup on /sys/fs/cgroup/blkio type cgroup (rw,nosuid,nodev,noexec,relatime,blkio)
cgroup on /sys/fs/cgroup/memory type cgroup (rw,nosuid,nodev,noexec,relatime,memory)
cgroup on /sys/fs/cgroup/perf_event type cgroup (rw,nosuid,nodev,noexec,relatime,perf_event)
cgroup on /sys/fs/cgroup/net_cls type cgroup (rw,nosuid,nodev,noexec,relatime,net_cls)
cgroup on /sys/fs/cgroup/freezer type cgroup (rw,nosuid,nodev,noexec,relatime,freezer)
cgroup on /sys/fs/cgroup/devices type cgroup (rw,nosuid,nodev,noexec,relatime,devices)
cgroup on /sys/fs/cgroup/hugetlb type cgroup (rw,nosuid,nodev,noexec,relatime,hugetlb)
cgroup on /sys/fs/cgroup/cpuset type cgroup (rw,nosuid,nodev,noexec,relatime,cpuset)
configfs on /sys/kernel/config type configfs (rw,relatime)
/dev/mapper/centos-root on / type xfs (rw,relatime,attr2,inode64,noquota)
systemd-1 on /proc/sys/fs/binfmt_misc type autofs (rw,relatime,fd=26,pgrp=1,timeout=300,minproto=5,maxproto=5,direct)
debugfs on /sys/kernel/debug type debugfs (rw,relatime)
hugetlbfs on /dev/hugepages type hugetlbfs (rw,relatime)
mqueue on /dev/mqueue type mqueue (rw,relatime)
/dev/xvda1 on /boot type xfs (rw,relatime,attr2,inode64,noquota)
tmpfs on /run/user/1000 type tmpfs (rw,nosuid,nodev,relatime,size=1497296k,mode=700,uid=1000,gid=1000)

Note: no non root fs non XFS

[centos@sebcm ~]$ cat /sys/kernel/mm/transparent_hugepage/enabled
always madvise [never]
[centos@sebcm ~]$ cat /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]

[centos@sebcm ~]$ cat /etc/hosts
127.0.0.1   localhost localhost.localdomain localhost4 localhost4.localdomain4
::1         localhost localhost.localdomain localhost6 localhost6.localdomain6

172.22.126.13  sebce.hadoop  sebce
172.22.164.97  sebcm.hadoop  sebcm
172.22.157.58 sebcw1.hadoop sebcw1
172.22.56.64  sebcw2.hadoop sebcw2
172.22.126.27 sebcw3.hadoop sebcw3

[centos@sebcm ~]$ ip addr
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN 
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc pfifo_fast state UP qlen 1000
    link/ether 02:eb:b0:61:79:c8 brd ff:ff:ff:ff:ff:ff
    inet 172.22.164.97/16 brd 172.22.255.255 scope global dynamic eth0
       valid_lft 3291sec preferred_lft 3291sec
    inet6 fe80::eb:b0ff:fe61:79c8/64 scope link 
       valid_lft forever preferred_lft forever

[centos@sebcm ~]$ for i in sebce sebcm sebcw1 sebcw2 sebcw3 ; do getent hosts $i ; done
172.22.126.13   sebce.hadoop sebce
172.22.164.97   sebcm.hadoop sebcm
172.22.157.58   sebcw1.hadoop sebcw1
172.22.56.64    sebcw2.hadoop sebcw2
172.22.126.27   sebcw3.hadoop sebcw3
[centos@sebcm ~]$ for i in 172.22.126.13 172.22.164.97 172.22.157.58 172.22.56.64 172.22.126.27 ; do getent hosts $i ; done
172.22.126.13   sebce.hadoop sebce
172.22.164.97   sebcm.hadoop sebcm
172.22.157.58   sebcw1.hadoop sebcw1
172.22.56.64    sebcw2.hadoop sebcw2
172.22.126.27   sebcw3.hadoop sebcw3

[centos@sebcm ~]$ systemctl status nscd
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; enabled; vendor preset: disabled)
   Active: active (running) since lun 2017-10-16 16:22:09 EDT; 7min ago
  Process: 662 ExecStart=/usr/sbin/nscd $NSCD_OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 668 (nscd)
   CGroup: /system.slice/nscd.service
           └─668 /usr/sbin/nscd

ott 16 16:22:09 sebcm.hadoop nscd[668]: 668 monitoring directory `/etc` (2)
ott 16 16:22:09 sebcm.hadoop nscd[668]: 668 monitoring file `/etc/resolv.con...)
ott 16 16:22:09 sebcm.hadoop nscd[668]: 668 monitoring directory `/etc` (2)
ott 16 16:22:09 sebcm.hadoop nscd[668]: 668 monitoring file `/etc/services` (6)
ott 16 16:22:09 sebcm.hadoop nscd[668]: 668 monitoring directory `/etc` (2)
ott 16 16:22:09 sebcm.hadoop nscd[668]: 668 disabled inotify-based monitorin...y
ott 16 16:22:09 sebcm.hadoop nscd[668]: 668 stat failed for file `/etc/netgr...y
ott 16 16:22:09 sebcm.hadoop systemd[1]: Started Name Service Cache Daemon.
ott 16 16:22:09 sebcm.hadoop nscd[668]: 668 monitored file `/etc/resolv.conf...h
ott 16 16:22:29 sebcm.hadoop nscd[668]: 668 checking for monitored file `/et...y
Hint: Some lines were ellipsized, use -l to show in full.

[centos@sebcm ~]$ systemctl status ntpd
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; enabled; vendor preset: disabled)
   Active: active (running) since lun 2017-10-16 16:22:09 EDT; 7min ago
  Process: 660 ExecStart=/usr/sbin/ntpd -u ntp:ntp $OPTIONS (code=exited, status=0/SUCCESS)
 Main PID: 681 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─681 /usr/sbin/ntpd -u ntp:ntp -g

ott 16 16:22:11 sebcm.hadoop ntpd_intres[683]: DNS 0.centos.pool.ntp.org -> ...0
ott 16 16:22:11 sebcm.hadoop ntpd_intres[683]: DNS 1.centos.pool.ntp.org -> ...9
ott 16 16:22:11 sebcm.hadoop ntpd_intres[683]: DNS 2.centos.pool.ntp.org -> ...7
ott 16 16:22:11 sebcm.hadoop ntpd_intres[683]: DNS 3.centos.pool.ntp.org -> ...8
ott 16 16:22:12 sebcm.hadoop ntpd[681]: Listen normally on 4 eth0 172.22.164...3
ott 16 16:22:12 sebcm.hadoop ntpd[681]: Listen normally on 5 eth0 fe80::eb:b...3
ott 16 16:22:12 sebcm.hadoop ntpd[681]: new interface(s) found: waking up re...r
ott 16 16:22:19 sebcm.hadoop ntpd[681]: 0.0.0.0 c61c 0c clock_step +0.965607 s
ott 16 16:22:20 sebcm.hadoop ntpd[681]: 0.0.0.0 c614 04 freq_mode
ott 16 16:22:22 sebcm.hadoop ntpd[681]: 0.0.0.0 c618 08 no_sys_peer
Hint: Some lines were ellipsized, use -l to show in full.
[centos@sebcm ~]$ 
