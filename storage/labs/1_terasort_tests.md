```
[ale966@sebcm ~]$ time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/jars/hadoop-examples.jar teragen -Dmapreduce.job.maps=4 -Ddfs.blocksize=33554432 100000000 /user/ale966/teragen

real    2m42.889s
user    0m6.144s
sys     0m0.248s

```
```
[ale966@sebcm ~]$ time hadoop jar /opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/jars/hadoop-examples.jar terasort  /user/ale966/teragen /user/ale966/terasort

real    8m54.437s
user    0m9.788s
sys     0m0.393s
```

