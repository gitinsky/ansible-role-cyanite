# Cyanite

This role expects that you install it to the host running cassandra that listens on ```{{ cassandra_node_iface_int }}``` interface.

This role is part of cyanite–cassandra–statsd–graphite-api–grafana installation and contains vagrant file to test the whole set. Please note that grafana role currently listens on http port 3000 (we use nginx with https as a frontend but it's ommitted in vagrant).

Graphite-api can connect to cyanite nodes by inventory_hostname or by ip, see defaults for more details.

# Reference
http://www.slideshare.net/planetcassandra/cassandra-summit-2014-cyanite-better-graphite-storage-with-apache-cassandra
