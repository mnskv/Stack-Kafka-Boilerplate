after extracting files
change server and zookeeper config path to actual path

Required Commands:

.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

.\bin\windows\kafka-server-start.bat .\config\server.properties

kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partition 1 --topic test

kafka-console-producer.bat --broker-list localhost:9092 --topic test
-------------------------------------------------------------------------------------------------------
Sample Data:

{"Name: "John", "Age":"31", "Gender":"Male"}
{"Name: "Emma", "Age":"27", "Gender":"Female"}
{"Name: "Ronald", "Age":"17", "Gender":"Male"}
---------------------------------------------------------------------------------------------------------

kafka-console-consumer.bat --topic test --bootstrap-server localhost:9092 --from-beginning
