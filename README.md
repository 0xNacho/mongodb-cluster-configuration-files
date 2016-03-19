# mongodb-cluster-configuration-files
This project contains all the config files needed by a sharded cluster. This is a very basic tutorial, and this cluster should be used just for testing and educational purposes.

##Query Router
``sudo mongos --config /etc/queryRouter.conf``

##Config Server
``sudo mongod --config /etc/configServer.conf``

##RPs and Shards
``sudo mongod --config /etc/shard.conf``

Once you've done tjat, you need to initiate your RPs:

``rs.initiate()``

``rs.conf()``

``rs.add("host:27017")``// add more hosts to RP



