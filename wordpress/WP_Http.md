# WP_Http

Core class used for managing HTTP transports and making HTTP requests. This class will automatically pick and use the transport API that is supported by the web host.

```php
<?php
if ( ! class_exists( 'WP_Http' ) ) {
    include_once( ABSPATH . WPINC . '/class-http.php' );
}

$request = new WP_Http;
$result  = $request->request( $url );
$json = $result['body'];

return $json;
```

