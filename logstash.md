apt install logstash

systemctl daemon-reload

systemctl enable logstash.service

systemctl start logstash.service

systemctl status logstash.service

nano /etc/logstash/conf.d/logstash.conf

systemctl restart logstash.service

systemctl status logstash.service

usermod -aG adm logstash

GET /_cat/indices
