# linux-cmds
Error : Err:4 https://packages.microsoft.com/repos/code stable InRelease                                                      
  The following signatures couldn't be verified because the public key is not available: NO_PUBKEY EB3E94ADBE122

  https://askubuntu.com/questions/1433368/how-to-solve-gpg-error-with-packages-microsoft-com-pubkey

wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
rm -f packages.microsoft.gpg



sudo mysql -u root -p

Stop sudo systemctl stop mysql
sudo systemctl start mysql
sudo mkdir -p /var/run/mysqld
sudo chmod 777 /var/run/mysqld
sudo mysqld_safe --skip-grant-tables --skip-networking &
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'Admin@2023!';
sudo systemctl status mysql
ps aux | grep mysql
sudo kill -9 6544 6545 6546 6718

