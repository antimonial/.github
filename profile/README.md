<p align="center"><a href="https://github.com/antimonial" target="_blank"><img src="https://raw.githubusercontent.com/antimonial/.github/main/profile/logo.png" width="120"></a></p>

<p align="center">
<a href="https://github.com/antimonial/framework/releases"><img src="https://img.shields.io/github/v/release/antimonial/framework?style=flat-square" alt="Latest Release"></a>
<a href="https://github.com/antimonial/framework/blob/main/LICENSE"><img src="https://img.shields.io/github/license/antimonial/framework?style=flat-square" alt="License"></a>
<a href="https://packagist.org/packages/antimonial/framework"><img src="https://img.shields.io/packagist/v/antimonial/framework?style=flat-square" alt="Packagist Version"></a>
</p>

## About Antimonial

Antimonial is a minimal, expressive PHP framework for server-rendered apps — no JavaScript dependencies by default.

We build tools for developers who want clarity and control — explicit code over implicit conventions, transparent SQL over hidden abstractions.

### Design Principles

- **No DI container** — import dependencies explicitly, like native PHP
- **No ORM** — QueryBuilder exposes transparent SQL you can understand and optimize
- **No template engine** — pure PHP views, extensible via `View::setEngine()` if you need one
- **No coupled services** — jobs, queues, mail, cache are delegated externally
- **Middleware via interfaces** — `MiddlewareInterface` + onion pattern, no Pipeline class
- **Zero JS dependencies** — the framework has no frontend opinions

### Getting Started

The fastest way to start a new app is the official skeleton:

```bash
composer create-project antimonial/antimonial my-app
cd my-app
php -S localhost:8000 -t public public/index.php
```

To add the framework to an existing Composer project instead:

```bash
composer require antimonial/framework
```

```php
<?php
define('ROOT_PATH', __DIR__ . '/..');
require ROOT_PATH . '/vendor/autoload.php';

Antimonial\Core\Config::load('app');
Antimonial\Core\Config::load('database');
Antimonial\Core\ErrorHandler::enableDebug(true);

$app = new Antimonial\Core\App();
$app->run();
```

### Packages

| Package | Description |
|---------|-------------|
| [`antimonial/framework`](https://github.com/antimonial/framework) | The core MVC framework |
| [`antimonial/antimonial`](https://github.com/antimonial/antimonial) | The starter application skeleton |

## Documentation

See the [framework README](https://github.com/antimonial/framework#readme) for full documentation, usage examples, and directory structure.

## License

Antimonial is open source software licensed under the [MIT license](https://github.com/antimonial/framework/blob/main/LICENSE).
