# run spark with docker 

apache/spark-py 10M
docker run -it apache/spark-py /opt/spark/bin/pyspark
spark.range(1000 * 1000 * 1000).count()

bitnami/spark 10M
https://hub.docker.com/r/bitnami/spark

docker run -it --rm \
    --name spark \
    -e SPARK_MODE=master \
    -p 8080:8080 \
    -p 7077:7077 \
    apache/spark-py
