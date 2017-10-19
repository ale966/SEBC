```
[ale966@sebce ~]$ kinit 
Password for ale966@HADOOP.COM: 
[ale966@sebce ~]$ klist
Ticket cache: FILE:/tmp/krb5cc_1001
Default principal: ale966@HADOOP.COM

Valid starting       Expires              Service principal
10/19/2017 11:45:05  10/20/2017 11:45:05  krbtgt/HADOOP.COM@HADOOP.COM
        renew until 10/26/2017 11:45:05
[ale966@sebce ~]$ beeline 

Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> 
beeline> !connect jdbc:hive2://localhost:10000/default;principal=hive/sebce.hadoop@HADOOP.COM
scan complete in 2ms
Connecting to jdbc:hive2://localhost:10000/default;principal=hive/sebce.hadoop@HADOOP.COM
Enter username for jdbc:hive2://localhost:10000/default;principal=hive/sebce.hadoop@HADOOP.COM: ale966
Enter password for jdbc:hive2://localhost:10000/default;principal=hive/sebce.hadoop@HADOOP.COM: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://localhost:10000/default> SHOW TABLES;
INFO  : Compiling command(queryId=hive_20171019114646_eae287dd-75be-4448-b14f-e8afabe38aa1): SHOW TABLES
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019114646_eae287dd-75be-4448-b14f-e8afabe38aa1); Time taken: 0.81 seconds
INFO  : Executing command(queryId=hive_20171019114646_eae287dd-75be-4448-b14f-e8afabe38aa1): SHOW TABLES
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019114646_eae287dd-75be-4448-b14f-e8afabe38aa1); Time taken: 0.288 seconds
INFO  : OK
+-----------+--+
| tab_name  |
+-----------+--+
+-----------+--+
No rows selected (2.411 seconds)
0: jdbc:hive2://localhost:10000/default> 
```
```
0: jdbc:hive2://localhost:10000/default> CREATE ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20171019114949_b9abd1c4-6258-4a82-b66e-8d81f8ad47ad): CREATE ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019114949_b9abd1c4-6258-4a82-b66e-8d81f8ad47ad); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20171019114949_b9abd1c4-6258-4a82-b66e-8d81f8ad47ad): CREATE ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019114949_b9abd1c4-6258-4a82-b66e-8d81f8ad47ad); Time taken: 0.724 seconds
INFO  : OK
No rows affected (0.801 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ALL ON SERVER server1 TO ROLE sentry_admin;
INFO  : Compiling command(queryId=hive_20171019114949_4fa85103-50bf-4ffe-b315-0a4d89b7c5fa): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019114949_4fa85103-50bf-4ffe-b315-0a4d89b7c5fa); Time taken: 0.084 seconds
INFO  : Executing command(queryId=hive_20171019114949_4fa85103-50bf-4ffe-b315-0a4d89b7c5fa): GRANT ALL ON SERVER server1 TO ROLE sentry_admin
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019114949_4fa85103-50bf-4ffe-b315-0a4d89b7c5fa); Time taken: 0.088 seconds
INFO  : OK
No rows affected (0.18 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ROLE sentry_admin TO GROUP ale966;
INFO  : Compiling command(queryId=hive_20171019115252_c4983961-712e-4f13-9839-d5748e94e684): GRANT ROLE sentry_admin TO GROUP ale966
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019115252_c4983961-712e-4f13-9839-d5748e94e684); Time taken: 0.067 seconds
INFO  : Executing command(queryId=hive_20171019115252_c4983961-712e-4f13-9839-d5748e94e684): GRANT ROLE sentry_admin TO GROUP ale966
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019115252_c4983961-712e-4f13-9839-d5748e94e684); Time taken: 0.071 seconds
INFO  : OK
No rows affected (0.147 seconds)
0: jdbc:hive2://localhost:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20171019115252_e70aa03f-ef93-4552-86af-e764f2c9490e): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019115252_e70aa03f-ef93-4552-86af-e764f2c9490e); Time taken: 0.061 seconds
INFO  : Executing command(queryId=hive_20171019115252_e70aa03f-ef93-4552-86af-e764f2c9490e): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019115252_e70aa03f-ef93-4552-86af-e764f2c9490e); Time taken: 0.126 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.24 seconds)
0: jdbc:hive2://localhost:10000/default> CREATE ROLE reads;
INFO  : Compiling command(queryId=hive_20171019115858_3e1a1272-32c8-4e5f-9a06-7672a16e1f1f): CREATE ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019115858_3e1a1272-32c8-4e5f-9a06-7672a16e1f1f); Time taken: 0.091 seconds
INFO  : Executing command(queryId=hive_20171019115858_3e1a1272-32c8-4e5f-9a06-7672a16e1f1f): CREATE ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019115858_3e1a1272-32c8-4e5f-9a06-7672a16e1f1f); Time taken: 0.048 seconds
INFO  : OK
No rows affected (0.148 seconds)
0: jdbc:hive2://localhost:10000/default> CREATE ROLE writes;
INFO  : Compiling command(queryId=hive_20171019115858_fc4899c7-4159-4fdb-a1f5-851f71da9b86): CREATE ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019115858_fc4899c7-4159-4fdb-a1f5-851f71da9b86); Time taken: 0.06 seconds
INFO  : Executing command(queryId=hive_20171019115858_fc4899c7-4159-4fdb-a1f5-851f71da9b86): CREATE ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019115858_fc4899c7-4159-4fdb-a1f5-851f71da9b86); Time taken: 0.029 seconds
INFO  : OK
No rows affected (0.096 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT SELECT ON DATABASE default TO ROLE reads;
INFO  : Compiling command(queryId=hive_20171019115858_26682371-c36d-4d98-9e82-a3c0d4020d70): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019115858_26682371-c36d-4d98-9e82-a3c0d4020d70); Time taken: 0.069 seconds
INFO  : Executing command(queryId=hive_20171019115858_26682371-c36d-4d98-9e82-a3c0d4020d70): GRANT SELECT ON DATABASE default TO ROLE reads
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019115858_26682371-c36d-4d98-9e82-a3c0d4020d70); Time taken: 0.039 seconds
INFO  : OK
No rows affected (0.125 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ROLE reads TO GROUP selector;
INFO  : Compiling command(queryId=hive_20171019115858_012bed7a-1417-4a52-8827-b5d6998103b0): GRANT ROLE reads TO GROUP selector
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019115858_012bed7a-1417-4a52-8827-b5d6998103b0); Time taken: 0.06 seconds
INFO  : Executing command(queryId=hive_20171019115858_012bed7a-1417-4a52-8827-b5d6998103b0): GRANT ROLE reads TO GROUP selector
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019115858_012bed7a-1417-4a52-8827-b5d6998103b0); Time taken: 0.03 seconds
INFO  : OK
No rows affected (0.099 seconds)
0: jdbc:hive2://localhost:10000/default> REVOKE ALL ON DATABASE default FROM ROLE writes;
INFO  : Compiling command(queryId=hive_20171019115858_6b091797-11f4-4836-b781-1b9df5876102): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019115858_6b091797-11f4-4836-b781-1b9df5876102); Time taken: 0.071 seconds
INFO  : Executing command(queryId=hive_20171019115858_6b091797-11f4-4836-b781-1b9df5876102): REVOKE ALL ON DATABASE default FROM ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019115858_6b091797-11f4-4836-b781-1b9df5876102); Time taken: 0.084 seconds
INFO  : OK
No rows affected (0.164 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT SELECT ON default.sample_07 TO ROLE writes;
INFO  : Compiling command(queryId=hive_20171019115959_7981585d-6cc0-46b4-aed8-b186169c8475): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019115959_7981585d-6cc0-46b4-aed8-b186169c8475); Time taken: 0.061 seconds
INFO  : Executing command(queryId=hive_20171019115959_7981585d-6cc0-46b4-aed8-b186169c8475): GRANT SELECT ON default.sample_07 TO ROLE writes
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019115959_7981585d-6cc0-46b4-aed8-b186169c8475); Time taken: 0.038 seconds
INFO  : OK
No rows affected (0.106 seconds)
0: jdbc:hive2://localhost:10000/default> GRANT ROLE writes TO GROUP inserters;
INFO  : Compiling command(queryId=hive_20171019115959_ab8458b7-81e7-4aff-9e9c-3af0aeed6288): GRANT ROLE writes TO GROUP inserters
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:null, properties:null)
INFO  : Completed compiling command(queryId=hive_20171019115959_ab8458b7-81e7-4aff-9e9c-3af0aeed6288); Time taken: 0.058 seconds
INFO  : Executing command(queryId=hive_20171019115959_ab8458b7-81e7-4aff-9e9c-3af0aeed6288): GRANT ROLE writes TO GROUP inserters
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019115959_ab8458b7-81e7-4aff-9e9c-3af0aeed6288); Time taken: 0.028 seconds
INFO  : OK
No rows affected (0.096 seconds)
0: jdbc:hive2://localhost:10000/default> 
```
```
[root@sebcm ~]# kinit george
Password for george@HADOOP.COM: 
[root@sebcm ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: george@HADOOP.COM

Valid starting       Expires              Service principal
10/19/2017 11:59:39  10/20/2017 11:59:39  krbtgt/HADOOP.COM@HADOOP.COM
        renew until 10/26/2017 11:59:39
[root@sebcm ~]# beeline 
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM
scan complete in 3ms
Connecting to jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM
Enter username for jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM: george
Enter password for jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://sebce.hadoop:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20171019120505_d7d04391-1483-4047-8e13-0621e29675d6): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019120505_d7d04391-1483-4047-8e13-0621e29675d6); Time taken: 0.073 seconds
INFO  : Executing command(queryId=hive_20171019120505_d7d04391-1483-4047-8e13-0621e29675d6): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019120505_d7d04391-1483-4047-8e13-0621e29675d6); Time taken: 0.132 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (0.318 seconds)
```
```
0: jdbc:hive2://sebce.hadoop:10000/default> !quit
Closing: 0: jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM
[root@sebcm ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: george@HADOOP.COM

Valid starting       Expires              Service principal
10/19/2017 11:59:39  10/20/2017 11:59:39  krbtgt/HADOOP.COM@HADOOP.COM
        renew until 10/26/2017 11:59:39
[root@sebcm ~]# kinit ferdinand
Password for ferdinand@HADOOP.COM: 
[root@sebcm ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: ferdinand@HADOOP.COM

Valid starting       Expires              Service principal
10/19/2017 12:07:48  10/20/2017 12:07:48  krbtgt/HADOOP.COM@HADOOP.COM
        renew until 10/26/2017 12:07:48
[root@sebcm ~]# beeline
Beeline version 1.1.0-cdh5.8.3 by Apache Hive
beeline> !connect jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM
scan complete in 2ms
Connecting to jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM
Enter username for jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM: ferdinad
Enter password for jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM: ********
Connected to: Apache Hive (version 1.1.0-cdh5.8.3)
Driver: Hive JDBC (version 1.1.0-cdh5.8.3)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://sebce.hadoop:10000/default> show tables;
INFO  : Compiling command(queryId=hive_20171019120808_67ae2379-4a9b-44d5-a79a-2b68bef48bc7): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20171019120808_67ae2379-4a9b-44d5-a79a-2b68bef48bc7); Time taken: 0.068 seconds
INFO  : Executing command(queryId=hive_20171019120808_67ae2379-4a9b-44d5-a79a-2b68bef48bc7): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20171019120808_67ae2379-4a9b-44d5-a79a-2b68bef48bc7); Time taken: 0.138 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| sample_07  |
+------------+--+
1 row selected (0.323 seconds)
0: jdbc:hive2://sebce.hadoop:10000/default> 
0: jdbc:hive2://sebce.hadoop:10000/default> !quit
Closing: 0: jdbc:hive2://sebce.hadoop:10000/default;principal=hive/sebce.hadoop@HADOOP.COM

```
