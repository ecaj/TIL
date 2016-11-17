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
Edit apache2 config file. For directory `/var/www/`, replace `AllowOverride None` with `AllowOverride All`.
```shell
sudo vim /etc/apache2/apache2.conf
```
Restart Apache2.
```shell
sudo service apache2 restart
```
Go to `http://server-address/dokuwiki/install.php` and start the initial configuration.
<br>
Delete `install.php` file.
```shell
sudo rm /var/www/html/dokuwiki/install.php
```

## Running multiple DokuWiki on a single machine.
Just install more DokuWiki into other subdirectories.
To share a single DokuWiki engine through multiple wikis, see [DokuWiki Farms](https://www.dokuwiki.org/farms)
>A wiki farm is a collection of wikis running on the same web server and sharing one parent wiki engine. So, by running just one single parent wiki, you can power hundreds of independent other wikis (aka “animals”). All animals share one set of plugins and templates but each of them can have a different set of enabled plugins, a different template and a different configuration. The concept of farms is also called “multi-site”, “multi-domain” or “sub-sites” in the context of other CMS.

## Troubleshooting



## Reference
- [DokuWiki - Installation](https://www.dokuwiki.org/install)