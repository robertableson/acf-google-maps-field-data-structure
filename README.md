# Advanced Custom Field (ACF) Google Maps field data structure

This is an example of the data structure to update through PHP the Advanced Custom Fields (ACF) plugin's Google Maps field.

Source: [AwesomeACF](https://www.awesomeacf.com/snippets/how-to-update-an-acf-google-map-field-programmatically-using-php/)

## Code

```PHP
<?php

// The field accepts a value with this structure
$value = [
    'address' => '123 Example St, Townsville XYZ 1234, Country',
    'lat' => – 38.1486228,
    'lng' => 144.360414,
    'zoom' => 14,
    'place_id' => 'Ei0xMjMgTW9vcmFib29sIFN0LCBHZWVsb25nIFZJQyAzMjIwLCBBdXN0cmFsaWEiMBIuChQKEgmX0JaIHBTUahFyH_LC9sYD8hB7KhQKEglDz-DYDxTUahECZY8QisCjzg',
    'street_number' => 123,
    'street_name' => 'Example Street',
    'street_name_short' => 'Example St',
    'city' => 'Townsville',
    'state' => 'Statename',
    'state_short' => 'XYZ',
    'post_code' => 1234,
    'country' => 'Country',
    'country_short' => 'ZX',
];

// If you need a new post, create one.
$post_id = wp_insert_post(['post_type' => 'post', 'post_status' => 'publish']);

// Update the ACF field for a given post.
update_field($field_name, $value, $post_id);
```