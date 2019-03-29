if on windows container change network to NAT 
on linux run bridge

run the docker-compose up in directory of docker-compose.yml
  this will get kafka manager and kafka server running
  
once running browse to http://localhost:9000 and you should see kafka manager

create a cluster
create a topic


TESTING:

download
https://www.apache.org/dyn/closer.cgi?path=/kafka/0.10.2.0/kafka_2.11-0.10.2.0.tgz

open command prompt to where you export the zip

look for bin\windows

modify hosts.etc to have 
127.0.0.1 kafkasertver

run kafka consumer

K:\kafka_2.11-0.10.2.0\bin\windows> .\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic NAME OF YOUR TOPIC

run kafka producer
K:\kafka_2.11-0.10.2.0\bin\windows> .\kafka-console-producer.bat --broker-list localhost:9092 --topic NAME OF YOUR TOPIC

to stop it 
docker-compose down where you have the yml
