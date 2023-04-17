apt install kibana

systemctl daemon-reload

systemctl enable kibana.service

systemctl start kibana.service

systemctl status kibana.service

nano /etc/kibana/kibana.yml

systemctl restart kibana

GET /_cluster/health?pretty
