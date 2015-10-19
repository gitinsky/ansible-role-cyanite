# Cyanite

This role expects that you install it to the host running cassandra that listens on ```{{ cassandra_node_iface_int }}``` interface.

This role is part of cyanite–cassandra–statsd–graphite-api–grafana installation and contains vagrant file to test the whole set. Please note that grafana role currently listens on http port 3000 (we use nginx with https as a frontend but it's ommitted in vagrant).

Graphite-api can connect to cyanite nodes by inventory_hostname or by ip, see defaults for more details.

If you use elasticsearch and cyanite fails to create index, use the following command:

```bash
curl -XPUT 'http://localhost:9200/cyanite/'
```

# Reference
http://www.slideshare.net/planetcassandra/cassandra-summit-2014-cyanite-better-graphite-storage-with-apache-cassandra

# Debug

## Cyanite

http://cyanitehost:8080/paths?query=*

## Graphite-api

http://graphiteapi:8001/metrics/find?query=*