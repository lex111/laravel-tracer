# Tracer

Tracer shows the paths of all the Blade files that are loaded into your templates. This could be very convenient for a number of reasons:
* If you're working on a large project with alot of views/partials
* New to a project and want to get a quick overview of the structure of pages
* If you're completely new to Laravel and want to play around with views/partials/templates etc.

![Screenshot](screenshot.png?raw=true)

## Installation

First install this package via Composer:
```sh
$ composer require appstract/laravel-tracer --dev
```

Then add the following class to your service providers list in `config/app.php` file:
```php
'providers' => [
    // ...
    Appstract\Tracer\TracerServiceProvider::class,
];
```

Publish the config file:
```sh
$ php artisan vendor:publish --provider="Appstract\Tracer\TracerServiceProvider"
```

A tracer.php file will be created in your `app/config` directory.


## Basic usage

In `app/config/tracer.php` file, if trace is set to true you see the paths of all the Blade files that are loaded into your templates. To remove the paths simply set trace to false. If your views are located at another directory you can set the correct path here.


### Toggle traces

A tracer.js file will be created in your `public/js` directory. This gets injected at the end of your app ```<head> ``` section.

Use the keybord shortcut ```ctrl+z ``` inside your app to toggle the traces.


## Testing

``` bash
$ composer test
```

## Contributing

Contributions are welcome, [thanks to y'all](https://github.com/appstract/laravel-tracer/graphs/contributors) :)

## About Appstract

Appstract is a small team from The Netherlands. <3 Laravel, Vue and other awesome tools.

## Buy us a beer

Would be awesome if you would [buy us a beer](https://www.paypal.me/teamappstract/10)! Or [a lot of beer](https://www.patreon.com/appstract) :)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
