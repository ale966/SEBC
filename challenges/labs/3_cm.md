```
[hdfs@chalm ~]$ hdfs dfs -ls /user
Found 6 items
drwx--x--x   - ernest  usa             0 2017-10-20 06:06 /user/ernest
drwxrwxrwx   - mapred  hadoop          0 2017-10-20 05:42 /user/history
drwxrwxr-t   - hive    hive            0 2017-10-20 05:43 /user/hive
drwxrwxr-x   - hue     hue             0 2017-10-20 05:44 /user/hue
drwxrwxr-x   - oozie   oozie           0 2017-10-20 05:44 /user/oozie
drwx--x--x   - siwicki emea            0 2017-10-20 06:05 /user/siwicki
```
```
curl -u admin:admin localhost:7180/api/v14/hosts
{
  "items" : [ {
    "hostId" : "af0df0f7-c981-4d92-a689-223672466efa",
    "ipAddress" : "172.22.53.133",
    "hostname" : "chale.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://chalm.hadoop:7180/cmf/hostRedirect/af0df0f7-c981-4d92-a689-223672466efa",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  }, {
    "hostId" : "87b60d1b-934e-47c9-b173-2f088d29e56a",
    "ipAddress" : "172.22.169.4",
    "hostname" : "chalm.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://chalm.hadoop:7180/cmf/hostRedirect/87b60d1b-934e-47c9-b173-2f088d29e56a",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  }, {
    "hostId" : "f9eb5a09-7302-4a06-b9d3-9d8db27b8735",
    "ipAddress" : "172.22.213.244",
    "hostname" : "chalw1.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://chalm.hadoop:7180/cmf/hostRedirect/f9eb5a09-7302-4a06-b9d3-9d8db27b8735",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  }, {
    "hostId" : "57bd536d-be60-42fc-8eaf-2b13393fe00d",
    "ipAddress" : "172.22.137.252",
    "hostname" : "chalw2.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://chalm.hadoop:7180/cmf/hostRedirect/57bd536d-be60-42fc-8eaf-2b13393fe00d",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  }, {
    "hostId" : "9a0ea431-1179-49a9-aacc-39fded72400e",
    "ipAddress" : "172.22.83.65",
    "hostname" : "chalw3.hadoop",
    "rackId" : "/default",
    "hostUrl" : "http://chalm.hadoop:7180/cmf/hostRedirect/9a0ea431-1179-49a9-aacc-39fded72400e",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 2,
    "totalPhysMemBytes" : 15332311040
  } ]
}
```
