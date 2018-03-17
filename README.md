# MediaServerRu

Setup rTorrent systemd  

sudo systemctl daemon-reload  
sudo service rtorrent start       - start  
sudo service rtorrent stop        - stop  


Create RuTorrent Password for nginx;  
sudo sh -c "echo -n 'scouseman:' >> /etc/nginx/.htpasswd"  
sudo sh -c "openssl passwd -apr1 >> /etc/nginx/.htpasswd"  
