This repository was forked from (GeneaLabs/laravel-nova-prepopulate-searchable)[https://github.com/GeneaLabs/laravel-nova-prepopulate-searchable] and they deserve all of the credit. We've only made minor changes to accommodate our software.

# Prepoulate Searchable for Laravel Nova
**A tool to allow BelongsTo searchable fields to be pre-populated with data**

[![Latest Version on Packagist](https://img.shields.io/packagist/v/genealabs/nova-prepopulate-searchable.svg?style=flat-square)](https://packagist.org/packages/alexbowers/nova-prepopulate-searchable)
[![Total Downloads](https://img.shields.io/packagist/dt/alexbowers/nova-prepopulate-searchable.svg?style=flat-square)](https://packagist.org/packages/genealabs/nova-prepopulate-searchable)

![Prepopulate Search](https://github.com/genealabs/nova-prepopulate-searchable/blob/master/screenshots/example.gif?raw=true)

## Sponsors
We thank the following sponsors for their generosity. Please take a moment to check them out:

- [LIX](https://lix-it.com)

## Requirements
- PHP 7.3+
- Laravel 7.0+
- Nova 3.8.4+

## Installation

You can install the package in to a Laravel app that uses [Nova](https://nova.laravel.com) via composer:

```bash
composer require oyova/laravel-nova-prepopulate-searchable
```

## Usage

On any `BelongsTo` fields in your resources that are `searchable()`, you can also add `prepopulate()` to the method chain and the field will be prepopulated with values to choose from.

You may optionally pass through a search query to the prepopulate method, and the keywords passed will be used for
the search initially, before resetting the search to being empty (as it currently is).

### Limiting Pre-Populated Items
You can limit the prepopulated items by passing in a search string to the `prepopulated()` method like so:

```php
    BelongsTo::make("Archive")
        ->searchable()
        ->prepopulate("test").
```

This would prepopulate all archives that have test in their display field.

### Security

If you discover any security related issues, please email hello@genealabs.com instead of using the issue tracker.

## Credits

### [Alex Bowers](https://github.com/alexbowers)

Alex is the original developer of this package and has done a great job with initial development.

### [Mike Bronner](https://github.com/mikebronner)

I started using this package and didn't want it to fall to the way-side, as it helps improve the UX of Nova significantly. Alex graceously allowed me to continue development and maintenance on his original package.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
