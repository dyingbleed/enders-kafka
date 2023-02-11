# Ender's Kafka

Apache Kafka Ansible Role

Setup local testing environment quickly and easily.

# Features

- \[DONE\] Kafka Cluster (with ZooKeeper)
- \[TODO\] Kafka Cluster (without ZooKeeper)
- \[TODO\] Kafka MirrorMaker
- \[DONE\] Kafka Connect
  - \[DONE\] MySQL Connector
  - \[TODO\] Elasticsearch Connector
- \[TODO\] AKHQ
- \[TODO\] JMX Exporter

# Variables

## Common Variables

- `scala_version`, Scala version, default is `2.1.3`
- `kafka_version`, Kafka version, default is `2.8.2`
- `kafka_home`, Kafka home directory, default is `/opt/kafka`
- `kafka_ip_address` **RECOMMENDED**, node external ip address

## ZooKeeper

- `zookeeper_version`, ZooKeeper version, default is `3.7.1`
- `zookeeper_home`, ZooKeeper home directory, default is `/opt/zookeeper`
- `zookeeper_data_dir`, ZooKeeper data directory, default is `/data/zookeeper`
- `zookeeper_log_dir`, ZooKeeper log directory, default is `/var/log/zookeeper`
- `zookeeper_myid` **REQUIRD**, `myid` for ZooKeeper

## Kafka

- `kafka_broker_log_dirs` Kafka broker log directories, default is `/data/kafka`
- `kafka_broker_id` **REQUIRD**, `broker_id` for Kafka

## Kafka Connect

- `kafka_connect_plugin_path` Kafka Connect plugin path, default is `/opt/connectors`

### MySQL Connector

Debezium connector for MySQL, check [here](https://debezium.io/documentation/reference/2.1/connectors/mysql.html).

- `mysql_connector_enable` if install MySQL connector, default is `no`
- `mysql_connector_version` MySQL connector version, default is `2.1.2.Final`

# Demo

Setup the VMs:

```
vagrant up
```

Deploy:

```
ansible-playbook deploy.yml
```
