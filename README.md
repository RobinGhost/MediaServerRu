# MediaServerRu

Setup rTorrent systemd;  


sudo systemctl enable rtorrent
sudo systemctl daemon-reload  
sudo service rtorrent start       - start  
sudo service rtorrent stop        - stop  


Create RuTorrent Password for nginx;  
sudo sh -c "echo -n 'scouseman:' >> /etc/nginx/.htpasswd"  
sudo sh -c "openssl passwd -apr1 >> /etc/nginx/.htpasswd"  

  
https://github.com/QuickBox/club-QuickBox


# Copying Completed Torrents
add new method to get finished dir


method.insert = d.get_finished_dir,simple,"cat=[folder]/finished/,$d.get_custom1="

method.set_key = event.download.finished,move_complete,"d.set_directory=$d.get_finished_dir=;execute=mkdir,-p,$d.get_finished_dir=;execute=mv,-u,$d.get_base_path=,$d.get_finished_dir="
