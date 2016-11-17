# Creating a first page fails
After clean install, clicking on `Create this page` redirects to a blank page.<br>
Apache2 error log: `PHP Fatal error:  Uncaught Error: Call to undefined function utf8_decode() in /var/www/dokuwiki/inc/utf8.php:152\nStack`

## Solution
Install php-xml.
```shell
sudo apt install php-xml
sudo service apache2 restart
```

## Reference
- [I only get a blank or partial page](https://www.dokuwiki.org/faq:blankpage)
- [utf8_(en|de)code removed from php7?](http://stackoverflow.com/questions/35701730/utf8-endecode-removed-from-php7)
- [DocuWiki and Ubuntu LTS 16.04](https://forum.dokuwiki.org/thread/13630)