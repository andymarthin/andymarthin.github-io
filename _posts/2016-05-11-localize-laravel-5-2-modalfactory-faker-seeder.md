---
layout: post
title: Localize Laravel 5.2 ModalFactory Faker Seeder
author: "Andy Marthin"
comments:  true
header-img: "img/laravel.jpg"
---
Beberapa waktu yang lalu ketika saya lagi "belajar" laravel, saya merasa kurang puas saat mengunakan faker saat seeder data. karena faker secara default mengukan "en_US" atau standart data amerika seperti nama, alamat, no telp, dll.

<!--more-->

ubah `/app/Providers/AppServiceProvider.php`

```php
use Faker\Generator as FakerGenerator;  
use Faker\Factory as FakerFactory;

...

function register( ) {  
  $this->app->singleton(FakerGenerator::class, function () {
      return FakerFactory::create('id_ID');
  });
}

...
```

atau ubah `/database/factories/ModelFactory.php`

```php

$faker = Faker\Factory::create('id_ID');

$factory->define(App\Employe::class, function () use ($faker){
	return[
		'name'        => $faker->name,
		'phonenumber' => $faker->phoneNumber,
		'email'       => $faker->freeEmail ,
		'address'     => $faker->streetAddress,
		'company'     => $faker->company,
	];
});

```

Thanks to [wlkns.co](http://wlkns.co/localize-laravel-5-2-factory-faker-seeder/)
