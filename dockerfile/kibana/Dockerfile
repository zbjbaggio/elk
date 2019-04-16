# Version: 0.0.1
FROM docker.elastic.co/kibana/kibana:6.2.4
MAINTAINER ZBJ "zhangbaojun@4zlink.com"
RUN cd /usr/share/kibana/bin
RUN ./kibana-plugin install https://search.maven.org/remotecontent?filepath=com/floragunn/search-guard-kibana-plugin/6.2.4-14/search-guard-kibana-plugin-6.2.4-14.zip
EXPOSE 5601