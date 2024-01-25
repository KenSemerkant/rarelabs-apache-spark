# rarelabs-apache-spark - steps for building a master with 2 workers spark 3.4.2

1) docker build -t rarelabs-apache-spark:3.4.2
2) docker scout quickview
3) docker-compose up -d

Test the build 
1) docker container ps
2) get the container id for master
3) docker exec -it <<container id>> /bin/bash
4) cd bin
5) ./spark-submit --master spark://0.0.0.0:7077 --name spark-pi --class org.apache.spark.examples.SparkPi  local:///opt/spark/examples/jars/spark-examples_2.12-3.4.2.jar 100
