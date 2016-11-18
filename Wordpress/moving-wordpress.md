# Moving WordPress
Needs to take caution when moving WordPress from one server to another. Follow these steps.

1. First, backup the database and the WordPress core files just in case.
2. Go to the **Administration > Settings > General Settings** panel and change **WordPress Address (URL)** and **Site Address (URL)** to the new URL. Save changes. At this point, the site may be broken and give a 404 page.
2. Backup the database again. Move this database and the WordPress core files to the new server.
3. Edit the database file. Search and replace previous URL to the new URL. On the new server, restore the database.
4. Access WordPress through the new URL and see if everything checks out.

## Reference
- [Moving WordPress](https://codex.wordpress.org/Moving_WordPress)