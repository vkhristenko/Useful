# Various Configuration options for launching Apache Spark

## YARN cluste mode
__To exit the process on the driver side right after submitting to the cluster__
```
spark-submit --master yarn --deploy-mode cluster --conf spark.yarn.submit.waitAppCompletion=false driver_convert2images.py
```
