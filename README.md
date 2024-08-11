## Kafka SASL plaintext auth docker compose setup

#### OS Tested on: Ubuntu 24.04

To set it up locally download all three files and place the `kafka-jaas.conf` and `zookeeper-jaas.con` inside `/etc/kafka/config` folder, if the folder does not exist then create it.
The config files do not have to be in this specific directory, you could place these files in your home directory as well for example and replace the path in the `docker-compose.yml` file.

Once the config files are in the right place just run following command to get the kafka containers up and running:

Run the following if using docker compose v2 plugin
```
docker compose up --build
```
Or, the following command if not using v2 plugin
```
docker-compose up --build
```

In your code use "test" as the value for both `username` and `password`.
