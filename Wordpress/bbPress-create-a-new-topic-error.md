# bbPress create a new topic error
## Problem
When creating a new topic, bbPress gives following error:
`ERROR: Are you sure you wanted to do that?`

## Solution

1. Create a child theme
2. Append following lines to the `functions.php` of the child theme:
```php
<?php
...
add_filter( 'bbp_verify_nonce_request_url', 'my_bbp_verify_nonce_request_url', 999, 1 );
function my_bbp_verify_nonce_request_url( $requested_url )
{
return 'https://server-address:port-number' . $_SERVER['REQUEST_URI'];
}
?>
```
Change `'https://server-address:port-number'` accordingly.

## Reference

[ERROR: Are you sure you wanted to do that?](https://bbpress.org/forums/topic/error-are-you-sure-you-wanted-to-do-that-3/#post-142468)