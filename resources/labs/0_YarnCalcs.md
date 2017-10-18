```
essentially I accept the values which comes from excel

OS node reserved memory could be execessive (12.8 GB) if yarn jobs are more cpu-bound than io-bound, because in the last case OS needs much memory for io cache

-workload factor: it's related to the number of map or reduce tasks that could run per job on each worker node. In this case a value of 1 for workload factor would limit mapreduce.job.maps and mapreduce.job.reduces values to 10 while any other value will not influence the value of 15 due to vcore and memory availability on each node

Optimal workload factor setting depends also on application use cases

```
