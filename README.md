# Blade Component

## What is blade in laravel?

Blade is the simple, yet powerful templating engine provided with Laravel. Unlike other popular PHP templating engines, Blade does not restrict you from using plain PHP code in your views. Blade view files use the .blade.php file extension and are typically stored in the resources/views directory.

## What is component in laravel?

Components are a reusable group of elements. Like you may want to create a Navbar to be used in almost all of your web-app pages. So you build your Navbar as a Component and tell laravel to grab it whenever you need it, and for many times as you like.

## Steps To Install And Use Blade Component

Install Fresh Laravel Project

#### composer create-project –prefer-dist laravel/laravel blade_component

Now, set up the database in the .env file.
We are going to see the Blade X using an Listing Users example. So we Will Use By Default Files Like HomeController. But Before It We Need To Install  
#### composer require laravel/ui and php artisan ui vue --auth
After that run  
#### php artisan migrate

For Create Component Run Following Command
#### php artisan make:component userlist 
It Will Create file inside app/views/component/userlist.php And resources/views/components/userlist.blade.php file

We need to make routes in the routes/web.php file
#### Route::get('/home','HomeController@index');

Also, we need to make functions in the App/Http/Controllers/HomeController.php file.
![homeindex](/public/homeindex.png)



First, we are going to write blade x tag Into resources/Views/home.blade.php file.
In home.blade.php file <x-userlist></x-userlist> tag userlist is component view file into 
resources/views/components/userlist.blade.php file.whatever data pass into <x-userlist> tag it will render into userlist.blade.php file.
![homeindexview](/public/homeindexview.png)
![homeindexcomponentview](/public/homeindexcomponentview.png)


In app\view\components\userlist.php file we need to pass $users variable into contruct method.
![homeindexcomponent1](/public/homeindexcomponent1.png)

For More Details Can Visit Following Link:- https://github.com/jigard/blade_component_laravel7

## Installation And Use

    $ git clone https://github.com/jigard/blade_component_laravel7

    $ cp .env.example .env
Change configuration according to your need in ".env" file and create Database
    
    $ composer install
    
    $ php artisan migrate
    
    $ php artisan serve


