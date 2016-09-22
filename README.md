# laravelAdmin
I am creating simple laravel project with QuickAdmin panel.

Please see below step to install within 10 mintus:-

1.) Fresh laravel installation using this command in CLI:  composer create-project laravel/laravel ProjectName --prefer-dist

2.) update composer : composer update 
then use this commnad : composer require laraveldaily/quickadmin

3.) Open to your \config\app.php file and Add this Laraveldaily\Quickadmin\QuickadminServiceProvider::class, 
after this line App\Providers\RouteServiceProvider::class, 

4.) Configure your .env file with correct database information

5.) Run php artisan quickadmin:install

6.) Open App\Http\Kernel.php file and Insert this line 'role' => \Laraveldaily\Quickadmin\Middleware\HasPermissions::class,
in $routeMiddleware

7.) Run php artisan serve 
Open browser and enter http://localhost/admin
