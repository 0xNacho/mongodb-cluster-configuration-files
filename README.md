# mongodb-cluster-configuration-files
This project contains all the config files needed by a sharded cluster. All the config are very basic, and should be used just for testing and educational purposes.

##Query Router
``sudo mongos --config /etc/queryRouter.conf``

##Config Server
``sudo mongod --config /etc/configServer.conf``

##Replica Sets
``sudo mongod --config /etc/shard.conf``


