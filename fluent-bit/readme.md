# Info
label: Fluent-Bit
version: latest

# Docker

## Pull
- `docker pull fluent/fluent-bit:latest`

## Image usage
- `docker run -ti --rm --name fluent-bit -v /Volumes/Docker/images/elk/fluent-bit:/etc/fluent-bit -v /Volumes/Data/www/sitesoft/bpextra/storage/logs:/var/logs fluent/fluent-bit /fluent-bit/bin/fluent-bit --config=/etc/fluent-bit/fluent.conf`

- `docker run -d --net efknet -u fluent -p 24224:24224 -p 24224:24224/udp --name fluentd fluentd`


`docker run -ti fluent/fluent-bit /fluent-bit/bin/fluent-bit -i cpu -o stdout`

`docker run -ti fluent/fluent-bit /fluent-bit/bin/fluent-bit -i cpu -t cpu -o es://localhost:9200/test/cpu \
    -o stdout -m '*'`
