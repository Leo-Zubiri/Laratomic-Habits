# First steps

## Acerca del proyecto

Laratomic Habits es un backend desarrollado con laravel con la posibilidad de ser consumido por el frontend de preferencia.

Inicios de sesión, registro de hábitos, envío de correos, gráficos, generación de documentos dinámicos y más.

El desarrollo de este proyecto es solo con fines de aprendizaje y práctica.

## Creación del proyecto

```bash
composer create-project laravel/laravel Laratomic-Habits
```

## Configuracion Inicial de DB

Desde el archivo `.env` es usual establecer los siguientes valores en los primeros pasos:

```bash title="Archivo .env"
APP_NAME="Laratomic Habits"
...
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laratomic
DB_USERNAME=root
DB_PASSWORD=MyPassword
```

Ejecutar: ```php artisan migrate```

> Lo anterior intenta crear las primeras tablas en la base de datos
