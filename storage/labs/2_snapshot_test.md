[ale966@sebcm ~]$ hdfs dfs -mkdir /user/ale966/precious

[ale966@sebcm ~]$ hdfs dfs -put /tmp/SEBC-master.zip /user/ale966/precious/

[ale966@sebcm ~]$ hdfs dfs -ls /user/ale966/precious/
Found 1 items
-rw-r--r--   3 ale966 ale966     450893 2017-10-17 09:51 /user/ale966/precious/SEBC-master.zip


[hdfs@sebcm ~]$ hdfs dfsadmin -allowSnapshot /user/ale966/precious
Allowing snaphot on /user/ale966/precious succeeded


[ale966@sebcm ~]$ hdfs dfs -createSnapshot /user/ale966/precious sebc-hdfs-test
Created snapshot /user/ale966/precious/.snapshot/sebc-hdfs-test


[ale966@sebcm ~]$ hdfs dfs -rm -skipTrash /user/ale966/precious/SEBC-master.zip
Deleted /user/ale966/precious/SEBC-master.zip

[ale966@sebcm ~]$ hdfs dfs -rmdir /user/ale966/precious
rmdir: The directory /user/ale966/precious cannot be deleted since /user/ale966/precious is snapshottable and already has snapshots

[ale966@sebcm ~]$ hdfs dfs -cp -ptopax /user/ale966/precious/.snapshot/sebc-hdfs-test/SEBC-master.zip /user/ale966/precious/


[ale966@sebcm ~]$ hdfs dfs -ls /user/ale966/precious
Found 1 items
-rw-r--r--   3 ale966 ale966     450893 2017-10-17 09:51 /user/ale966/precious/SEBC-master.zip

