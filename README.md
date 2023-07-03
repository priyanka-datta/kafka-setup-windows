# kafka-setup-windows
For setting up kafka on windows machine the below steps need to be followed.<br/>
  1. Need to download Kafka.
  2. Extract it in C drive and rename it as Kafka.
  3. In Kafka folder, there are 2 folders bin and config.
  4. In config folder, need to go to zookeeper.properties file and edit the datadir as C:/Kafka/zookeeper-data.
  5. In config folder, need to go to server.properties file and edit the log.dir as C:/Kafka/kafka-logs.
  6. Need to open command prompt in C:/Kafka directory and run below command for starting zookeeper<br/><br/>
   ```      .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties          ```<br/>

  7. Need to open command prompt in C:/Kafka directory and run below command for starting kafka server<br/><br/>
   ```      .\bin\windows\kafka-server-start.bat .\config\server.properties            ```<br/>

  8. Need to open command prompt in C:/Kafka/bin/windows directory and run below command for setting up producer <br/><br/>
          i) Create a topic using below command<br/>
           ```      kafka-topics.bat --create --bootstrap-server localhost:9092 --topic <topic-name>     ```<br/><br/>
          ii)Connect kafka producer console for sending message using below command<br/>
            ```      kafka-console-producer.bat --broker-list localhost:9092 --topic test      ```<br/><br/>
  9. Need to open command prompt in C:/Kafka/bin/windows directory and run below command for opening console for consumer <br/>
   ```       kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning            ```<br/>

 10. For mentioning number of partitions to an existing topic need to open command prompt in C:/Kafka directory and run below command<br/>
   ```       .\bin\windows\kafka-topics.bat --bootstrap-server localhost:9092 --alter --topic test --partitions 2        ```
   
   
