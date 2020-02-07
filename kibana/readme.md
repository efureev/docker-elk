# Info
label: Kibana
version: 7.0.1

# Docker

## Image run
- `docker network create efknet`
- `docker run -d --name kibana --net efknet -p 5601:5601 docker.elastic.co/kibana/kibana:7.0.1`
