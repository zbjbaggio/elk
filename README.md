使用docker搭建基于6.2.4版本的elk日志搜集<br>
dockerfile文件夹下是相应的dockerfile文件安装了相应插件<br>

##filebeat<br>
docker run --name filebeat-6.2.4 -v /home/docker/filebeat-6.2.4/config/filebeat.yml:/usr/share/filebeat/filebeat.yml -v /home/logs/:/mnt/ -v /home/docker/filebeat-6.2.4/prospectors.d/:/usr/share/filebeat/prospectors.d/ -v /home/docker/filebeat-6.2.4/modules.d/:/usr/share/filebeat/modules.d/  -d filebeat-6.2.4 <br>

##logstash<br>
docker run -d -p 5044:5044 -p 10515:10515 -p 9600:9600 --name logstash-6.2.4 -v /home/docker/logstash-6.2.4/config:/usr/share/logstash/config -v /home/docker/logstash-6.2.4/pipeline:/usr/share/logstash/pipeline -v /home/docker/logstash/data:/home logstash-6.2.4 <br>

##elasticsearch<br>
docker run -d -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" --restart always --name es_1 -v /home/docker/elasticsearch/es_1/config:/usr/share/elasticsearch/config -v /home/docker/elasticsearch/es_1/data:/usr/share/elasticsearch/data elasticsearch:6.2.4 <br>

##kibana<br>
docker run --name kibana -v /home/docker/kibana-6.2.4/config:/usr/share/kibana/config -p 5601:5601 -d kibana-6.2.4<br>