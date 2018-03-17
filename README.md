# MediaServerRu

Create RuTorrent Password for nginx;
sudo sh -c "echo -n 'scouseman:' >> /etc/nginx/.htpasswd";
sudo sh -c "openssl passwd -apr1 >> /etc/nginx/.htpasswd";
