@webiste: http://foostart.com

@package-name: sample
@author: Kang
@date: 27/12/2017
@version: 2.0

@features

1. CRUD
2. Add category to form
3. Language standard
4. Add filters on table data
5. Add token for prevent XSRF

Step 1: Add service providers to config/app.php
Foostart\Contact\ContactServiceProvider::class,
Foostart\Slideshow\SlideshowServiceProvider::class,
Foostart\Filemanager\FilemanagerServiceProvider::class,Intervention\Image\ImageServiceProvider::class,

Step 2: Install publish
php artisan vendor:publish --provider="Foostart\Contact\ContactServiceProvider" --force
php artisan vendor:publish --provider="Foostart\Slideshow\SlideshowServiceProvider" --force

Step 3: And add class aliases
'Image' => Intervention\Image\Facades\Image::class,

Step 4: Publish the package’s config and assets :
php artisan vendor:publish --tag=lfm_config
php artisan vendor:publish --tag=lfm_public