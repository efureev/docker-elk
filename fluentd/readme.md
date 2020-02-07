# Info
label: Fluentd
version: edge

# Docker

## Build image
- `docker build --rm -t fluentd .`

## Image usage
- `docker run -d --net efknet -u fluent -p 24224:24224 -p 24224:24224/udp --name fluentd fluentd`


`docker run -ti fluent/fluent-bit /fluent-bit/bin/fluent-bit -i cpu -o stdout`
`docker run -ti fluent/fluent-bit /fluent-bit/bin/fluent-bit -i cpu -o stdout`

`docker run -ti fluent/fluent-bit /fluent-bit/bin/fluent-bit -i cpu -t cpu -o es://localhost:9200/test/cpu \
    -o stdout -m '*'`
