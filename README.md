# datapipeline1
This project focused on the setup and configuration of a data pipeline consisting of Kafka, Spark, and Hadoop.

https://github.com/kingan/datapipeline1


Setup Kafka

Download the tarball file

        http://ftp.heanet.ie/mirrors/www.apache.org/dist/kafka/0.9.0.1/kafka-0.9.0.1-src.tgz

Create the log directories

        /usr/local/kafka/logs/kafka_logs_1
        /usr/local/kafka/logs/kafka_logs_2
        /usr/local/kafka/logs/kafka_logs_2

Adjust the configuration file

        /usr/local/kafka/config/server1.properties
        /usr/local/kafka/config/server2.properties
        /usr/local/kafka/config/server3.properties

Launch zookeeper

        bin/zookeeper-server-start.sh config/zookeeper.properties &

Launch kafka server

        bin/kafka-server-start.sh config/server1.properties &
        bin/kafka-server-start.sh config/server2.properties &
        bin/kafka-server-start.sh config/server3.properties &

Create a kafka topic

        bin/kafka-topics.sh --zookeeper localhost:2181 --create --partitions 2 --replication-factor 2 --name first



