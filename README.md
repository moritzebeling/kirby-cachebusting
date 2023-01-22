# Kirby Cachebusting, CDN friendly

⚠️ This is taken from the Kirby website and source code and only here to simplify installation for myself via composer. Plese check:

https://getkirby.com/docs/cookbook/extensions/kirby-loves-cdn#cache-busting
https://github.com/getkirby/getkirby.com/blob/main/site/plugins/cdn/src/Cachebuster.php

The plugin adds a finderprint like `file.css?v=12345678` to every file added from the `/assets` folder using on of the Kirby helper methods like `css()` or `js()`.

## Setup

```php
# site/config/config.php
return [
    'moritzebeling.kirby-cachebusting' => false // to switch off completely,
    'moritzebeling.kirby-cachebusting.host' => 'https://remote-host.com', // to set remote host, like cdn
    // ...
];
```