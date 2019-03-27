# Version: 0.0.1
FROM docker.elastic.co/elasticsearch/elasticsearch:6.2.4
MAINTAINER ZBJ "zhangbaojun@4zlink.com"
USER root
RUN cd /usr/share/elasticsearch
RUN ./bin/elasticsearch-plugin install https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v6.2.4/elasticsearch-analysis-ik-6.2.4.zip
RUN ./bin/elasticsearch-plugin install com.floragunn:search-guard-6:6.2.4-23.0
RUN chmod 755 ./plugins/search-guard-6/tools/install_demo_configuration.sh
RUN ./plugins/search-guard-6/tools/install_demo_configuration.sh
EXPOSE 9200
