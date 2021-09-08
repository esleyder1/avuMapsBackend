# Laravel REST API con Sanctum

Api para la aplicación AVU maps
## Usage

Cambie el archivo *.env.example* a *.env* y agrega la información de la base de datos

crea la base de datos en phpmyadmin con el nombre:  avu_map_db 
y modificac el archivo .env con la configuración que tengas. 
ya está la configuración por defecto


```
DB_CONNECTION=sqlite
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=avu_map_db
```

Ejecute esta linea de código para instalar las dependencias
```
composer install
```
Ejecute esta linea de código para generar la KEY de la aplicación
```
php artisan key:generate
```
Ejecute esta linea de código para correr las migraciones 
```
php artisan migrate --seed
php artisan db:seed
```

```
# Corra la aplicación con el siguiente comando
php artisan serve
```


## Rutas del API

```
# Publicas

GET   /api/products
GET   /api/products/:id

POST   /api/login
@body: email, password

POST   /api/register
@body: name, email, password, password_confirmation


# Protegidas

POST   /api/products
@body: name, slug, description, price

PUT   /api/products/:id
@body: ?name, ?slug, ?description, ?price

DELETE  /api/products/:id

POST    /api/logout
```

### ejemplo
http://127.0.0.1:8000/api/login

Autor: Esleyder Ordoñez