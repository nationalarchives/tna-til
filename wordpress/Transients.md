# Transients API

Stores cached data in the database temporarily.

```php
<?php
$transient  = get_transient( 'html_content' );

if( !empty( $transient ) ) {

    echo $transient;
    
} else {

    $html = '<p>$content</p>';
    
    set_transient( 'html_content', $html, MONTH_IN_SECONDS );
    
    echo $html;
}
```
References:

https://codex.wordpress.org/Transients_API