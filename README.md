system
======


Cassandra 
-----------------
```bash
sudo apt-get update
sudo apt-get install openjdk-7-jdk -y
java -version

echo "deb http://debian.datastax.com/community stable main" | sudo tee -a /etc/apt/sources.list.d/cassandra.sources.list
curl -L http://debian.datastax.com/debian/repo_key | sudo apt-key add -
sudo apt-get update
apt-get install dsc20
service cassandra stop
rm -rf /var/lib/cassandra/data/system/*
service cassandra start
```

After installation

```bash
cassandra-cli
[default@unknown] create keyspace pyhackers;
<guid>
[default@unknown] show api version;
19.38.0
```
