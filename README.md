# mongodb-cluster-configuration-files
This project contains all the config files needed by a sharded cluster. This is a very basic tutorial, and this cluster should be used just for testing and educational purposes.

##Query Router
``sudo mongos --config /etc/queryRouter.conf``

##Config Server
``sudo mongod --config /etc/configServer.conf``

##RPs
``sudo mongod --config /etc/shard.conf``

Once you've done that, you need to initiate your RPs. Connect to a host, that will be your PRIMARY node on your RP:

``rs.initiate()``

``rs.conf()``

``rs.add("host:27017") // add more hosts to RP``

##Shards
Connect to a mongos instance:

``sh.addShard("rp1/host1:27017,host2:27017");``

``sh.addShard("rp2/host3:27017,host4:27017");``

Sharded cluster should be ready to use :)
