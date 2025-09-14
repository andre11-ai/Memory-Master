# Memory Master - Laravel Backend

Esta es la aplicación Laravel 12 para Memory Master, que proporciona autenticación de usuarios y será la base para las futuras funcionalidades del juego.

## Requisitos

- PHP 8.2 o superior
- Composer 2.x
- Node.js 18 o superior
- MySQL 5.7 o superior

## Instalación

1. Navegar al directorio Laravel:
   ```bash
   cd laravel
   ```

2. Copiar el archivo de configuración de ejemplo:
   ```bash
   cp .env.example .env
   ```

3. Configurar las credenciales de MySQL en el archivo `.env`:
   ```
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=memory_master
   DB_USERNAME=root
   DB_PASSWORD=
   ```

4. Instalar las dependencias de PHP:
   ```bash
   composer install
   ```

5. Generar la clave de aplicación:
   ```bash
   php artisan key:generate
   ```

6. Ejecutar las migraciones de base de datos:
   ```bash
   php artisan migrate
   ```

7. Instalar las dependencias de Node.js:
   ```bash
   npm install
   ```

8. Compilar los assets:
   ```bash
   npm run dev
   ```

9. Iniciar el servidor de desarrollo:
   ```bash
   php artisan serve
   ```

## Uso

1. Abrir el navegador y ir a `http://127.0.0.1:8000`
2. El sistema redirigirá automáticamente a la página de login si no estás autenticado
3. Registrar una nueva cuenta o iniciar sesión con una cuenta existente
4. Después del login, serás redirigido al panel de control (dashboard)

## Funcionalidades Implementadas

- ✅ Autenticación completa (registro, login, logout)
- ✅ Restablecimiento de contraseña por correo electrónico
- ✅ Verificación de correo electrónico (opcional)
- ✅ Interfaz completamente en español
- ✅ Configuración para MySQL
- ✅ Dashboard básico para usuarios autenticados
- ✅ Redirección automática según estado de autenticación

## Estructura del Proyecto

- `app/` - Modelos, controladores y middleware de la aplicación
- `resources/views/` - Vistas Blade (todas traducidas al español)
- `routes/web.php` - Definición de rutas web
- `lang/es/` - Archivos de traducción al español
- `database/migrations/` - Migraciones de base de datos

## Próximas Fases

En las siguientes fases se integrará:
- La interfaz del juego Memory Master existente
- Sistema de puntajes y estadísticas
- Modelos adicionales para el juego
