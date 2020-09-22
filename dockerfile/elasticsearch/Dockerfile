# Version: 0.0.1
FROM docker.elastic.co/elasticsearch/elasticsearch:6.2.4
MAINTAINER ZBJ "zhangbaojun@4zlink.com"
USER root
RUN cd /usr/share/elasticsearch \
    && ./bin/elasticsearch-plugin install https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v6.2.4/elasticsearch-analysis-ik-6.2.4.zip \
    && ./bin/elasticsearch-plugin install com.floragunn:search-guard-6:6.2.4-23.0 \
    && chmod 755 ./plugins/search-guard-6/tools/install_demo_configuration.sh \
    && ./plugins/search-guard-6/tools/install_demo_configuration.sh
EXPOSE 9200
