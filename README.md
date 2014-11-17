# Docker image for elasticsearch
The image is build in docker registry : https://registry.hub.docker.com/u/snasello/elasticsearch/
you can pull it :
```
docker pull snasello/elasticsearch
```

## Start image

you can start it directly
```
docker run --rm -it -p 9200:9200 snasello/elasticsearch
```
you have 9200 for http and 9300 for transport client

if you want to pass parameters:
```
docker run --rm -it -p 9200:9200 snasello/elasticsearch /elasticsearch/bin/elasticsearch --cluster.name=local --index.number_of_replicas=0 --discovery.zen.ping.multicast.enabled=false
```

## Install a plugin
docker exec <container_id|container_name> /elasticsearch/bin/plugin --install mobz/elasticsearch-head

