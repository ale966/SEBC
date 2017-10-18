```
$ curl -u ale966:cloudera http://localhost:7180/api/version
v14

$ curl  -u ale966:cloudera http://localhost:7180/api/v14/users
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "ale966",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}

$ curl  -u ale966:cloudera http://localhost:7180/api/v14/cm/scmDbInfo
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```
