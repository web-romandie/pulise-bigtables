## Big tables card for Laravel Pulse

This card will show you big tables in your database.

### Installation

You can install the package via composer:

```shell
composer require standapp/pulse-bigtable
```

### Publish the config file

```shell
php artisan vendor:publish --tag=pulse-bigtable
```

### Register the recorder
You must add the bigtable recorder to your `config/pulse.php` file:

```php
return [
    // ...
    'recorders' => [
         \StandApp\PulseBigTable\Recorders\BigTableRecorder::class => [],
  ],
]
```
You must also run the `php artisan pulse:check` command.

### Add the card to your dashboard

In your dashboard view, you can use the `bigtable` card type:

```php
<x-pulse>
    // ....
    <livewire:big-table cols='6' />
</x-pulse>
```

That's it! You should now see the big tables card on your pulse dashboard.
