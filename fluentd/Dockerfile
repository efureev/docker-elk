FROM fluent/fluentd:edge

LABEL Description="Listern filebeat messages on UDP port and send them into elasticsearch" Vendor="Feugene"

# ENV FLUENTD_ES_PLUGIN_VERSION="3.4.3"

# Use root account to use apk
USER root

# below RUN includes plugin as examples elasticsearch is not required
# you may customize including plugins as you wish
RUN apk add --no-cache --update --virtual .build-deps \
        build-base ruby-dev \
 && gem install fluent-plugin-elasticsearch \
 && gem sources --clear-all \
 && apk del .build-deps \
 && rm -rf /home/fluent/.gem/ruby/2.5.0/cache/*.gem


RUN set -xe \
  && gem install fluent-plugin-elasticsearch --no-rdoc --no-ri \
  ##--version ${FLUENTD_ES_PLUGIN_VERSION} \
  && fluentd --version

#COPY ./fluent.conf /fluentd/etc/fluent.conf

EXPOSE 5160/udp

USER fluent
