# Version: 0.0.1
FROM docker.elastic.co/logstash/logstash:6.2.4
MAINTAINER ZBJ "zhangbaojun@4zlink.com"
RUN cd /usr/share/logstash
RUN bin/logstash-plugin install logstash-filter-multiline
RUN bin/logstash-plugin install logstash-filter-date
RUN bin/logstash-plugin install logstash-filter-grok
RUN bin/logstash-plugin install logstash-filter-geoip
RUN bin/logstash-plugin install logstash-filter-mutate
