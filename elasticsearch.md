apt update && apt install -y wget gpg ca-certificates 

wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo gpg --dearmor -o /usr/share/keyrings/elasticsearch-keyring.gpg

echo "deb [trusted=yes signed-by=/usr/share/keyrings/elasticsearch-keyring.gpg] https://mirror.yandex.ru/mirrors/elastic/7/ stable main" | tee /etc/apt/sources.list.d/elastic-7.x.list

apt update && apt info elasticsearch

systemctl daemon-reload

systemctl enable elasticsearch.service

systemctl start elasticsearch.service

systemctl status elasticsearch.service
