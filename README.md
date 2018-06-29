
***************start kafka server**************
~/kafka/bin/kafka-server-start.sh ~/kafka/config/server.properties

************* create topic test *******************
bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic test

*************** afficher la liste des topics**************
bin/kafka-topics.sh --list --zookeeper localhost:2181

************ produce messages ********************** 
bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test

****************** consume messages ****************
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning


