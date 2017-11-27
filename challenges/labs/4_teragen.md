```
 time hadoop jar /opt/cloudera/parcels/CDH/jars/hadoop-mapreduce-examples-2.6.0-cdh5.9.3.jar teragen -Ddfs.blocksize=33554432 -Dmapreduce.job.maps=6 51200000 /user/ernest/tgen512m 

real    1m18.896s
user    0m6.137s
sys     0m0.312s


```

```
[ernest@chalm ~]$ hdfs dfs -ls /user/ernest/tgen512m
Found 7 items
-rw-r--r--   3 ernest usa          0 2017-10-20 06:23 /user/ernest/tgen512m/_SUCCESS
-rw-r--r--   3 ernest usa  853333400 2017-10-20 06:23 /user/ernest/tgen512m/part-m-00000
-rw-r--r--   3 ernest usa  853333300 2017-10-20 06:23 /user/ernest/tgen512m/part-m-00001
-rw-r--r--   3 ernest usa  853333300 2017-10-20 06:23 /user/ernest/tgen512m/part-m-00002
-rw-r--r--   3 ernest usa  853333400 2017-10-20 06:23 /user/ernest/tgen512m/part-m-00003
-rw-r--r--   3 ernest usa  853333300 2017-10-20 06:23 /user/ernest/tgen512m/part-m-00004
-rw-r--r--   3 ernest usa  853333300 2017-10-20 06:23 /user/ernest/tgen512m/part-m-00005
```
.
