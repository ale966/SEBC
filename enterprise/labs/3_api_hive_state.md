```
$ curl -u ale966:cloudera -X POST 'http://localhost:7180/api/v1/clusters/ale966/services/hive/commands/stop'
{
  "id" : 564,
  "name" : "Stop",
  "startTime" : "2017-10-18T13:55:49.060Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }

$ curl -u ale966:cloudera -X GET 'http://localhost:7180/api/v1/clusters/ale966/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://sebce.hadoop:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STOPPED",
  "healthSummary" : "DISABLED",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "DISABLED"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "DISABLED"
  } ],
  "configStale" : false

$ curl -u ale966:cloudera -XPOST 'http://localhost:7180/api/v1/clusters/ale966/services/hive/commands/start'
{
  "id" : 567,
  "name" : "Start",
  "startTime" : "2017-10-18T13:56:22.225Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}

$ curl -u ale966:cloudera -XGET 'http://localhost:7180/api/v1/clusters/ale966/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://sebce.hadoop:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTING",
  "healthSummary" : "DISABLED",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "DISABLED"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "DISABLED"
  } ],
  "configStale" : false
}

$ curl -u ale966:cloudera -X GET 'http://localhost:7180/api/v1/clusters/ale966/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://sebce.hadoop:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false
}
```
