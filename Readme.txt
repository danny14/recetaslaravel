1) Agregar la autentificacion del laravel desde la version 6 se empezo a implementar aparte
y se agrega con "composer require laravel/ui", despues "php artisan ui:auth" para habilitarlo, 
2) que son las migraciones, son como el control de version de nuestra base de datos, se puede modificar
y compartir el esquema de la base de datos, crear un migracion al crear un modelo, se le dice que campos va a 
tener la base de datos, "php artisan make:model Clientes --migration o --m" las migracions dan forma a los datos
estan los bigIncrements (PK), char, float, integer, string , text (mas grande que un varchar),
php artisan migrate. y despues php artisan migrate:rollback
3) agregarle estilos a la pagina, esta boostrap, vue, react, para instalar bootstrap solo basta
darle en "php artisan ui bootstrap" - "php artisan ui vue" -  npm install  - npm run dev, npm i vue-loader,
vamos a cambiarle el estilo al proyecto como tal, entonces vamos a "resource/sass/ _variables o app.scss,
acomodar en el package.json el vue-loader a version "vue-loader": "^15.9.8",
4) en layouts del login cambianos el bg-white por bg-primary,
despues buscamos unas fuentes en google fonts, en este caso fredoka y didactic gothic las importamos
en la app.scss y creamos una variable llamada "$parrafos-font-family"
5) php artisan tinker, y nos abre una shell
podemos insertar datos en la aplicacion y correr algun
query o select y mirar si funciona
entonces, creamos $usuario = new User;
$usuario->name = "Pepito";
$usuario->email = "correo@correo.com";
$usuario->password = Hash::make('12345678');
$usuario->save();

User::all(); -> trae todos los usuarios
User::find(1) o User::find(2) y se trae un solo usuario

todo esto gracias a eloquent que es un ORM, y a los modelos