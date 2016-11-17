# Install DokuWiki on Ubuntu Server 16.04 LTS

LAMP stack was already installed.
```shell
sudo apt install lamp-server^
```
Enable apache2 rewrite module
```shell
sudo a2enmod rewrite
```
Install DokuWiki by downloading the latest stable release.
```shell
cd /var/www/html
sudo wget http://download.dokuwiki.org/src/dokuwiki/dokuwiki-stable.tgz
sudo tar xvf dokuwiki-stable.tgz
sudo mv dokuwiki-*/ dokuwiki
sudo chown -R www-data:www-data dokuwiki
```
Edit apache2 config file.
```shell
sudo vim /etc/apache2/apache2.conf
```. For directory `/var/www/`, replace `AllowOverride None` with `AllowOverride All`.
Restart 


## Reference
- [DokuWiki - Installation](https://www.dokuwiki.org/install)