# List of users who have created at least one post using WP_User_Query

WP_User_Query is a class that allows querying WordPress database tables 'wp_users' and 'wp_usermeta'.

Useful when querying users who have created at least one post.

```php
<?php
function get_blog_list_authors() {

	$args = array(
		'has_published_posts' => true,
		'orderby' => 'display_name',
		'order'   => 'ASC'
	);
	$wp_user_query = new WP_User_Query( $args );
	$authors = $wp_user_query->get_results();

	foreach ( $authors as $author ) :

		echo '<li class="user-id-' . esc_html( $author->ID ) . '">' . esc_html( $author->display_name ) . '</li>';

	endforeach;
}
```

References:

https://codex.wordpress.org/Class_Reference/WP_User_Query
