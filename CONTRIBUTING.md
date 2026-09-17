# Contributing

Use PHP 8.3 or later and Composer, with the rasterizers described in
[Installation](docs/installation.md). Run `composer install`, then:

```sh
php vendor/bin/php-cs-fixer fix --dry-run --diff --sequential
composer sa
composer test
```

`composer cs` applies changes; use the dry-run command to check formatting.
Exercise SVG and PNG inputs with available adapters, and distinguish unavailable
adapter checks from passes. Verify image sizes, created/skipped statuses,
force behavior, public URL prefixes, and optional manifest output.

Documentation example assets are original MIT-licensed illustrations. Regenerate
the example with `php bin/favicon docs/assets/example/source.svg --output
docs/assets/example/generated --public-path /favicons --force`. The preview
uses relative URLs instead of the deployment prefix. Update guides and the
changelog when changing public behavior.
