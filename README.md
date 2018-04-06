# MediaServerRu

Setup rTorrent systemd;  


sudo systemctl enable rtorrent@8091  
sudo systemctl daemon-reload  
sudo service rtorrent start@8091         - start  
sudo service rtorrent stop@8091           - stop  


Create RuTorrent Password for nginx;  
sudo sh -c "echo -n 'scouseman:' >> /etc/nginx/.htpasswd"  
sudo sh -c "openssl passwd -apr1 >> /etc/nginx/.htpasswd"  

  
https://github.com/QuickBox/club-QuickBox


# Copying Completed Torrents
add new method to get finished dir


method.insert = d.get_finished_dir,simple,"cat=/srv/dev-disk-by-id-ata-ST4000VN008-2DR166_ZDH2PWQQ-part1/Downloads/seeding/,$d.get_custom1="

    
method.set_key = event.download.finished,move_complete,"d.set_directory=/srv/dev-disk-by-id-ata-ST4000VN008-2DR166_ZDH2PWQQ-part1/Downloads/seeding;execute=mkdir,-p,$d.get_finished_dir=;execute=cp,-rpl,$d.get_base_path=,$d.get_finished_dir="

