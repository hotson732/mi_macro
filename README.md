Para comenzar el trabajo necesitan tener varias cosas instaladas para instalarlo 

Linux configuración 
- Git Descargar(https://git-scm.com/)
- Node.js ≥ 20 Descargar(https://nodejs.org/)
- PHP ≥ 8.1 [Descargar](https://www.php.net/)
- Composer [Descargar](https://getcomposer.org/)

 Base de datos (opcional):
 PostgreSQL 

 Instalación en Linux (Ubuntu/Debian)

 1. Instalar dependencias del sistema:
bash
Actualizar sistema
sudo apt update && sudo apt upgrade -y

Instalar PHP y extensiones
sudo apt install php php-curl php-mbstring php-xml php-mysql php-sqlite3 php-zip

Instalar Node.js
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs

Instalar Composer
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer

git clone https://github.com/hotson732/mi_macro.git
cd mi_macro


Windows & Mac configuracion

Node + Npm ≥ 20 https://nodejs.org/es/download/
PHP 8.1 https://windows.php.net/download/
Composer https://getcomposer.org/download/



Configuracion en laravel para el proyecto (Ojo solo lo van a tener que hacer en su dispositivo esto no se hace commit ya que puede generar errores)
 directorio backend
cd backend

 dependencias PHP
composer install

Copiar archivo de entorno
cp .env.example .env

Generar key de la aplicación
php artisan key:generate

Configurar base de datos (editar .env)
DB_CONNECTION=sqlite (para SQLite)
 o configurar PostgreSQL


Ejecutar migraciones
php artisan migrate

Instalar Laravel Sanctum (para API)
php artisan sanctum:install

Ejecutar servidor de desarrollo (Solo es para su vista)
php artisan serve


Configuracion para react (Ojo solo lo van a tener que hacer en su dispositivo esto no se hace commit ya que puede generar errores)
Navegar al directorio frontend
cd frontend

 Instalar dependencias JavaScript
npm install

 Copiar archivo de entorno
cp .env.example .env

Configurar API URL (editar .env)
 REACT_APP_API_URL=http://localhost:8000/api

Ejecutar servidor de desarrollo
npm start


APP_URL=http://localhost:8000
FRONTEND_URL=http://localhost:3000

Backend (.env):
APP_URL=http://localhost:8000
FRONTEND_URL=http://localhost:3000

DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_PORT=5432
DB_DATABASE=mi_macro
DB_USERNAME=tu usuario de posgres 
DB_PASSWORD=tu contraseña de posgres


Frontend (.env):
REACT_APP_API_URL=http://localhost:8000/api


tener varios servicios activos para su funcionamiento
Terminal 1 - Backend
cd backend && php artisan serve

 Terminal 2 - Frontend  
cd frontend && npm start

Producción
Build frontend:
cd frontend
npm run build

Developer
hotson732 - GitHub

Cuando hagan commits los .env NO SE SUBEN YA QUE CONTIENEN INFORMACION IMPORTANTE Y UNICA EN CADA DISPOSITIVO ESTO GENERA FALLOS Y VULNERABILIDADES DE SEGURIDAD COMPLETAS EN EL PROYECTO
