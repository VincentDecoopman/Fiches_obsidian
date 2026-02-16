Lancer un serveur laravel : 
```shell
php artisan serve
```

Déterminer une route (URL précise) :
Dans le fichier /routes/web.php :
```php
Route::get('/login', [AuthController::class, 'showlogin'])->name('login');
```

Le /login sera l'url, donc une fois le serveur lancer, taper dans la barre d'URL 
"http://127.0.0.1:8000/login" 