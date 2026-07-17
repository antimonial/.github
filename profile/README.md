<p align="center"><a href="https://github.com/antimonial" target="_blank"><img src="https://raw.githubusercontent.com/antimonial/.github/main/profile/logo.png" width="120"></a></p>

<p align="center">
<a href="https://github.com/antimonial/framework/releases"><img src="https://img.shields.io/github/v/release/antimonial/framework?style=flat-square" alt="Latest Release"></a>
<a href="https://github.com/antimonial/framework/blob/main/LICENSE"><img src="https://img.shields.io/github/license/antimonial/framework?style=flat-square" alt="License"></a>
<a href="https://packagist.org/packages/antimonial/framework"><img src="https://img.shields.io/packagist/v/antimonial/framework?style=flat-square" alt="Packagist Version"></a>
</p>

## About Antimonial

A PHP MVC framework where what you read is what runs.

We build tools for developers who want clarity and control — explicit code over implicit conventions, transparent SQL over hidden abstractions.

### What's in the box

- **Template engine with automatic escaping** — safe output by default, no scattering `htmlspecialchars` through your views.
- **Router with named routes and regex params** — reverse them with the `route()` helper and match segments with patterns.
- **Typed QueryBuilder** — you read the SQL, you tune the SQL.
- **Sessions and CSRF** wired into the request cycle out of the box.
- **Middleware through interfaces** — implement `MiddlewareInterface` and wrap the app like an onion. No pipeline DSL.
- **PHPStan at max level** and a full test suite running in CI.

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
