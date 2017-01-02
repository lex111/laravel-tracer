# Tracer

Tracer shows the paths of all the blade files that are loaded into your templates. This could be very convenient for a number of reasons; If you're working on a large project with alot of views/partials. New to a project and want to get a quick overview of the structure of pages. Or if you're completely new to Laravel and want to play around with views/partials/templates etc.


## Installation

```sh
composer require rokr/tracer --dev
```

First do the composer install then add the following class to your config/app.php service providers list.
```sh
Rokr\Tracer\TracerServiceProvider::class,
```

Publish the config and tracer.js files
```sh
php artisan vendor:publish
```
A tracer.php file will be created in your app/config directory.

A tracer.js file will be created in your public/js directory.
Add the script to your HTML head section.
```sh
<script type="text/javascript" src="{{ asset('js/tracer.js') }}"></script>
```

## Basic Usage

In app/config tracer.php file, if trace is set to true you see the paths of all the blade files that are loaded into your templates. To remove the paths simply set trace to false. If your views are located at another directory you can set the correct path here.

## Toggle tracer shortcut

Use the keybord combination ```ctrl+z ``` inside the browser to toggle the traces in your app.

