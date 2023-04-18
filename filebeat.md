apt install filebeat

systemctl daemon-reload

systemctl enable filebeat.service

systemctl start filebeat.service

systemctl stop logstash.service

filebeat modules enable nginx
 
filebeat modules enable elasticsearch
  
filebeat modules enable kibana  

curl -X GET "localhost:9200/_cat/indices?pretty"

find /etc/filebeat/modules.d/ -iname '*.yml' -printf "%s %f\n" | sort -n
