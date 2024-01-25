# rarelabs-apache-spark - steps for building a master with 2 workers spark 3.4.2

1) docker build -t rarelabs-apache-spark:3.4.2
2) docker scout quickview
3) docker-compose up -d
4) docker container ps
5) get the container id for master
6) docker exec -it <<container id>> /bin/bash
7) cd bin
8) ./spark-submit --master spark://0.0.0.0:7077 --name spark-pi --class org.apache.spark.examples.SparkPi  local:///opt/spark/examples/jars/spark-examples_2.12-3.4.2.jar 100
9) 
