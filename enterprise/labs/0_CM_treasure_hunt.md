* What is ubertask optimization?
It can be applied to small mapreduse jobs which run sequentially in a single JVM. The properties which identify jobs subjected to such an optimization are: mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytesd

* Where in CM is the Kerberos Security Realm value displayed?
Going in CM:  Administration > Settings and searching the string "default_realm"

* Which CDH service(s) host a property for enabling Kerberos authentication?
Each CDH service starting from HDFS has a property for Kerberos enabling: YARN, Zookeeper, Oozie, Hive, Hue

* How do you upgrade the CM agents?
It could be done both manually installing Cloudera Manager Agent packages or by using the upgrade wizard invoked from Admin Console

* Give the tsquery statement used to chart Hue's CPU utilization?
select cpu_user_rate +  cpu_system_rate where serviceName=HUE

* Name all the roles that make up the Hive service
HiveServer2 Hive Metastore Server  WebHCat Server Gateway

* What steps must be completed before integrating Cloudera Manager with Kerberos?
As stated in https://www.cloudera.com/documentation/enterprise/5-8-x/topics/cm_sg_intro_kerb.html, the following steps are to be executed before launching CM Kerberos integration:

  * Set up a working KDC (MIT KDC or Active Directory)
  * Configure allowing of renewable tickets with non-zero ticket lifetimes by the KDC
  * Kerberos client/libs must be installed on ALL hosts in the cluster.
  * Create an account for Cloudera Manager that has the permissions to create other accounts in the KDC
