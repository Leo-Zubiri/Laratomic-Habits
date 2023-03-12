# Autenticación con Breeze

```bash
composer require laravel/breeze --dev
```

## Breeze & Next.js / API

```bash
php artisan breeze:install api
 
php artisan migrate
```

> Breeze agrega `FRONTENT_URL` a las variables de entorno en el archivo `.env`, típicamente es `http://localhost:3000`


Existe una plantilla para trabajar con Breeze con NextJS si no es necesario comenzar desde cero [`Visitar aqui->`](https://github.com/laravel/breeze-next)


## Activar verificación de Email

En el modelo User se debe agregar el implements en la clase:

```php title="Modelo User"
class User extends Authenticatable implements MustVerifyEmail
```
Y desde el endpoint en el archivo `api.php`:

```php
Route::middleware(['auth:sanctum','verified'])->get('/user', function (Request $request) {
    return $request->user();
});

```

> Para probar el correo de verificación se debe utilizar `Mailhog`