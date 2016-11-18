# Sync files between servers with rsync
```shell
rsync -avuz --progress /var/www/wordpress/ root@192.168.1.10:/var/www/wordpress/
```

## Useful options
```shell
-v, --verbose               increase verbosity
-a, --archive               archive mode; equals -rlptgoD (no -H,-A,-X)
-r, --recursive             recurse into directories
-l, --links                 copy symlinks as symlinks
-p, --perms                 preserve permissions
-t, --times                 preserve modification times
-g, --group                 preserve group
-o, --owner                 preserve owner (super-user only)
-D                          same as --devices --specials
    --devices               preserve device files (super-user only)
    --specials              preserve special files
-u, --update                skip files that are newer on the receiver
-z, --compress              compress file data during the transfer
    --progress              show progress during transfer
```

## Reference
- [rsync(1) - Linux man page](https://linux.die.net/man/1/rsync)