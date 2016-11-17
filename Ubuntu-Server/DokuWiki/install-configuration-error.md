# Install congfiguration error
After installing DokuWiki, visiting the install.php page gives following error:

>The installer found some problems, indicated below. You can not continue until you have fixed them.
>
>    * PHP function utf8_decode is not available. Maybe your hosting provider disabled it for some reason?


## Solution
```shell
sudo apt install php-mbstring
```

## Reference
- [install.php error php](https://forum.dokuwiki.org/thread/6641)