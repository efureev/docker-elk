# Info
label: Elasticsearch
version: 7.0.1

# Docker

## Image usage
- `docker network create efknet`
- `docker run -d -p 9200:9200 -p 9300:9300 --net efknet --name elasticsearch -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.0.1`
