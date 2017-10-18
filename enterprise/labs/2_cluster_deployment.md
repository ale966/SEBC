```
{
  "timestamp" : "2017-10-18T13:41:36.352Z",
  "clusters" : [ {
    "name" : "ale966",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "895483904"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "895483904"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2683672985"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "451"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "sebce.hadoop"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "metastorepassword"
        }, {
          "name" : "hive_metastore_database_user",
          "value" : "metastoreuser"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "d1qggzl0u2x94qabeo6tluh7y"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2bmccig680fyvu6hr094r236c"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "536870912"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-2db9cd18fdc9f6416320c9a0d104a618",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "e117f746-cd0d-4d04-a7f3-ac1ef895705e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "njxv367jfp6585a9f7dbt73q"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "66lb8dxzkqkdmwug9gzeimvta"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-ddeeee2cdffa8908b2db810dea111f82",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "d62fe390-5132-4f8a-a19c-f42291f90cf1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "crhcw46vbu0vokxawsehqwdxw"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "sebce.hadoop"
        }, {
          "name" : "database_password",
          "value" : "huepassword"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "database_user",
          "value" : "hueuser"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-cb1bb03a2fd9ddb2c9f02b5e775db5ae"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8wkhzhm8m7kc6jajv8v1gvpvn"
          }, {
            "name" : "secret_key",
            "value" : "RiiJMA1myxxznJzKrRG7ZerpCW0h4U"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "sebce.hadoop"
          }, {
            "name" : "oozie_database_password",
            "value" : "ooziepassword"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozieuser"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "536870912"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8tqicgioen8vvtlcpkp3eibcc"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3608"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3608"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "uEYuWUcqMvlOeOOlp5aHMXfvLPXmXJ"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-GATEWAY-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-2db9cd18fdc9f6416320c9a0d104a618",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "e117f746-cd0d-4d04-a7f3-ac1ef895705e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2qkpoti52ki779rkiuyib9s0g"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-7dfe33000b54a26b14bd1b017d574ef4",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "08001d4b-8e37-48ec-b286-1014685de3c7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1h4uuf4ei1onz9r37m6xhqk0d"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-bc1ed9d910c2bfcf5147dff4bfa5313d",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "6582fd95-1f86-40d0-9ae4-1c37ba4a4152"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "68p51n8x6ygsrekpo143g45p"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-ddeeee2cdffa8908b2db810dea111f82",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "d62fe390-5132-4f8a-a19c-f42291f90cf1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8m23ths1ybx16oe3x9e7mpdr4"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-2db9cd18fdc9f6416320c9a0d104a618",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "e117f746-cd0d-4d04-a7f3-ac1ef895705e"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "42"
          }, {
            "name" : "role_jceks_password",
            "value" : "2j46y8sqoarxiseqxwrjvexg9"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "2947575398"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "LPB1HB0rOk0SaMlZPPVFlcfxRcCtFs"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "w97TKYyprThc5LEmbdJImHIj3DlmEG"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "ZBAE927hjGFdr8lX5dAPJH1GvJClxb"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-7dfe33000b54a26b14bd1b017d574ef4",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "08001d4b-8e37-48ec-b286-1014685de3c7"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-7dfe33000b54a26b14bd1b017d574ef4",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "08001d4b-8e37-48ec-b286-1014685de3c7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7ymyqbtw4wnw39xl7q9szeaxh"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-bc1ed9d910c2bfcf5147dff4bfa5313d",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "6582fd95-1f86-40d0-9ae4-1c37ba4a4152"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3x9qaj6osjei78uwi7ez5gdvd"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-ddeeee2cdffa8908b2db810dea111f82",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "d62fe390-5132-4f8a-a19c-f42291f90cf1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ey8dfmybvaf7ru46hciix3hzk"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-2db9cd18fdc9f6416320c9a0d104a618",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "e117f746-cd0d-4d04-a7f3-ac1ef895705e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7bvi1r9sotrls6vo28274xj6o"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-bc1ed9d910c2bfcf5147dff4bfa5313d",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "6582fd95-1f86-40d0-9ae4-1c37ba4a4152"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3edlaqr5t7fe3a5vfru7chdio"
          } ]
        }
      }, {
        "name" : "hdfs-GATEWAY-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-HTTPFS-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "euse1m0cmg1qn5szsyip5d4mr"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-2db9cd18fdc9f6416320c9a0d104a618",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "e117f746-cd0d-4d04-a7f3-ac1ef895705e"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1iwcv6a8yo89h41v0v4k24we3"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-7dfe33000b54a26b14bd1b017d574ef4",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "08001d4b-8e37-48ec-b286-1014685de3c7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7mrsqdm6gt2k7qhydkef5gz19"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-ddeeee2cdffa8908b2db810dea111f82",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "d62fe390-5132-4f8a-a19c-f42291f90cf1"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "15u7es1tat7x4kzuxb3fc32kp"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-2db9cd18fdc9f6416320c9a0d104a618",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "e117f746-cd0d-4d04-a7f3-ac1ef895705e"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "sebc"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "sebc"
          }, {
            "name" : "namenode_id",
            "value" : "44"
          }, {
            "name" : "role_jceks_password",
            "value" : "7xdjcv50nf4h71b7l8vdbohg9"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-bc1ed9d910c2bfcf5147dff4bfa5313d",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "6582fd95-1f86-40d0-9ae4-1c37ba4a4152"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "sebc"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "sebc"
          }, {
            "name" : "namenode_id",
            "value" : "49"
          }, {
            "name" : "role_jceks_password",
            "value" : "791mdm34m3yfp5n4ixi731qyq"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94",
    "ipAddress" : "172.22.126.13",
    "hostname" : "sebce.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "e117f746-cd0d-4d04-a7f3-ac1ef895705e",
    "ipAddress" : "172.22.164.97",
    "hostname" : "sebcm.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "6582fd95-1f86-40d0-9ae4-1c37ba4a4152",
    "ipAddress" : "172.22.157.58",
    "hostname" : "sebcw1.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "08001d4b-8e37-48ec-b286-1014685de3c7",
    "ipAddress" : "172.22.56.64",
    "hostname" : "sebcw2.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "d62fe390-5132-4f8a-a19c-f42291f90cf1",
    "ipAddress" : "172.22.126.27",
    "hostname" : "sebcw3.hadoop",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__327b64c1-5ed8-43ac-bb4a-153afcff4dea",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "ce61cd63bff686a2d7d8d2e9e5b712f02c0416fb5df5889fdd015a0fbd208161",
    "pwSalt" : -3771890680699212347,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "62cad4367d482f0a795fa76e1fd3f4e9c3dcc0a7588bedc1442dd1a4da37d13c",
    "pwSalt" : -4021187808221473483,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "e819c8203a7861496c819fe0372dfe84b70aebdfeaf3f0faf5fe21875f6510c3",
    "pwSalt" : -8573477651283215626,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "0d86f581d7841097b33fb51cf87b9afe26a751eef2151247a0aaa60396120e60",
    "pwSalt" : -4299597667686005184,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "50a45c1e15568019df3d4ba7422f93622c0fa70ed63f3b225b1fa7a1915d5aa9",
    "pwSalt" : 7272753078449919759,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "4fedfbede41524504c908355b1b29b6bc371737d9fa1c1f7b2f921033575a71a",
    "pwSalt" : -2386807502120478573,
    "pwLogin" : true
  }, {
    "name" : "ale966",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "148277beb47da3f73e90075c4d76ca6b1dc14dcff670c12ab1ab947ec143dfd4",
    "pwSalt" : -507472204062958862,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "f36e4bee0950d1bcf9b69243ea5da5da233780c2c54455839b2ca19cfeccfff3",
    "pwSalt" : -2126239259940519912,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.8.3",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20161019-1013",
    "gitHash" : "518f0d6d44abc87bc392646e4369a20c8192b7cf",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "268435456"
        } ]
      }, {
        "roleType" : "ALERTPUBLISHER",
        "items" : [ {
          "name" : "alert_heapsize",
          "value" : "134217728"
        } ]
      }, {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "268435456"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "NAVIGATOR",
        "items" : [ {
          "name" : "navigator_heapsize",
          "value" : "268435456"
        } ]
      }, {
        "roleType" : "NAVIGATORMETASERVER",
        "items" : [ {
          "name" : "navigator_heapsize",
          "value" : "536870912"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "sebce.hadoop"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rmanpassword"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rmanuser"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "895483904"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "ctc0he8hsdxkye66mfpzr25l9"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6mqyhfjude5dzzbqksh9ckmf7"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4mrlodn0t97980vmxfi7cb8fq"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8kfnqpatkqpn0uh0kaprqvs6g"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-cb1bb03a2fd9ddb2c9f02b5e775db5ae",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "95441d8b-a35d-4fa9-9166-b64bce118d94"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6e0vt4f9qukhzj6898xjzvxxh"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 4:20"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "NOT_ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/5.8.3,http://sebce.hadoop/gplextras5/parcels/5.8.3,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}
```
