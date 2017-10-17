[hdfs@sebcm ~]$ hdfs fsck /user/ale966 -files -blocks 
Connecting to namenode via http://sebcm.hadoop:50070
FSCK started by hdfs (auth:SIMPLE) from /172.22.164.97 for path /user/ale966 at Tue Oct 17 08:08:09 EDT 2017
/user/ale966 <dir>
/user/ale966/_SUCCESS 0 bytes, 0 block(s):  OK

/user/ale966/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-291980758-172.22.164.97-1508196954175:blk_1073743119_2295 len=134217728 Live_repl=3
1. BP-291980758-172.22.164.97-1508196954175:blk_1073743120_2296 len=115782272 Live_repl=3

/user/ale966/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-291980758-172.22.164.97-1508196954175:blk_1073743118_2294 len=134217728 Live_repl=3
1. BP-291980758-172.22.164.97-1508196954175:blk_1073743121_2297 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Oct 17 08:08:09 EDT 2017 in 2 milliseconds


The filesystem under path '/user/ale966' is HEALTHY




[hdfs@sebcm ~]$ hdfs fsck /user/g0dj4ck4l -files -blocks 
Connecting to namenode via http://sebcm.hadoop:50070
FSCK started by hdfs (auth:SIMPLE) from /172.22.164.97 for path /user/g0dj4ck4l at Tue Oct 17 07:59:31 EDT 2017
/user/g0dj4ck4l <dir>
/user/g0dj4ck4l/_SUCCESS 0 bytes, 0 block(s):  OK

/user/g0dj4ck4l/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-291980758-172.22.164.97-1508196954175:blk_1073743314_2490 len=134217728 Live_repl=3
1. BP-291980758-172.22.164.97-1508196954175:blk_1073743317_2493 len=115782272 Live_repl=3

/user/g0dj4ck4l/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-291980758-172.22.164.97-1508196954175:blk_1073743313_2489 len=134217728 Live_repl=3
1. BP-291980758-172.22.164.97-1508196954175:blk_1073743316_2492 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    1
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          3
 Number of racks:               1
FSCK ended at Tue Oct 17 07:59:31 EDT 2017 in 3 milliseconds


The filesystem under path '/user/g0dj4ck4l' is HEALTHY

