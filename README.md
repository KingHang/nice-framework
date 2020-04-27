Nice PHP microframework
=========================

```php
<?php

use Symfony\Component\HttpFoundation\Request;
use Symfony\Component\HttpFoundation\Response;
use Nice\Application;
use Nice\Router\RouteCollector;

require __DIR__ . '/../vendor/autoload.php';

$app = new Application();
$app->set('routes', function (RouteCollector $r) {
    $r->map('/', 'home', function (Request $request) {
        return new Response('Hello, world');
    });
});
$app->run();
```


Documentation
-------------

View [the online documentation](http://docs.niceframework.com), or the check out the
[markdown documentation source code](https://github.com/nice-php/docs).
