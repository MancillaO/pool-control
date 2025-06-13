<div align="center">
    
# 🏊 Pool Control

![PHP Version](https://img.shields.io/badge/PHP-8.1%2B-777BB4?style=for-the-badge&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)

Sistema de gestión integral para el control de albercas y membresías.

</div>

## 📋 Requisitos Previos

| Requisito | Versión |
|-----------|---------|
| PHP | 8.1 o superior |
| Composer | Última estable |
| PostgreSQL | 12 o superior |
| Node.js | 16.x o superior (Opcional) |
| NPM | 8.x o superior (Opcional) |

## 🚀 Instalación Rápida

Sigue estos pasos para configurar el proyecto en tu entorno local:

### 1. Clonar el Repositorio

```bash
git clone https://github.com/MancillaO/pool_control.git
cd pool_control
```

### 2. Configuración del Entorno

1. Copia el archivo `.env.example` y renómbralo a `.env` (puedes hacerlo desde el Explorador de Windows o usando el comando en PowerShell):
   ```powershell
   Copy-Item .env.example .env
   ```

2. Abre el archivo `.env` en tu editor de texto preferido (como Notepad, VS Code, etc.) y configura las variables de entorno:
   ```env
   # Configuración de la base de datos PostgreSQL
   DB_CONNECTION=pgsql
   DB_HOST=127.0.0.1
   DB_PORT=5432
   DB_DATABASE=nombre_base_datos
   DB_USERNAME=tu_usuario
   DB_PASSWORD=tu_contraseña
   ```

### 3. Instalar Dependencias

1. Abre una terminal (PowerShell o Símbolo del sistema) y navega a la carpeta del proyecto.

2. Genera una nueva clave de aplicación:
   ```powershell
   php artisan key:generate
   ```

3. Instala las dependencias de Composer:
   ```powershell
   composer install
   ```

4. Instala AdminLTE (panel de administración):
   ```powershell
   php artisan adminlte:install
   ```

### 4. Configuración de la Base de Datos

1. Crea una base de datos PostgreSQL vacía usando pgAdmin o la herramienta de tu preferencia.

2. Ejecuta las migraciones y seeders (asegúrate de que el servicio de PostgreSQL esté en ejecución):
   ```powershell
   php artisan migrate:fresh --seed
   ```
   
   > ℹ️ Esto creará todas las tablas necesarias y cargará datos de prueba.

### 5. Iniciar la Aplicación

1. Inicia el servidor de desarrollo de Laravel:
   ```powershell
   php artisan serve
   ```
   
   > 💡 Si el puerto 8000 está en uso, puedes especificar otro puerto con: `php artisan serve --port=8080`

2. Abre tu navegador web favorito y visita:
   ```
   http://localhost:8000
   ```
   
   > 🔍 Si usaste un puerto diferente, asegúrate de usarlo en la URL (ej: `http://localhost:8080`)

## 🔑 Credenciales por Defecto

Se crea un usuario administrador con las siguientes credenciales:

- **Email:** admin@example.com
- **Contraseña:** password

> ⚠️ **Importante:** Cambia estas credenciales después del primer inicio de sesión.

## 🛠️ Comandos Útiles en Windows

| Comando | Descripción |
|---------|-------------|
| `php artisan serve` | Inicia el servidor de desarrollo |
| `php artisan migrate` | Ejecuta las migraciones pendientes |
| `php artisan db:seed` | Ejecuta los seeders |
| `php artisan optimize:clear` | Limpia la caché de la aplicación |
| `php artisan storage:link` | Crea el enlace simbólico para el almacenamiento |
| `php artisan queue:work` | Procesa trabajos en cola (si se usan) |

> 📝 **Nota para Windows:** Asegúrate de que PHP esté agregado al PATH del sistema o abre la terminal desde la carpeta donde está instalado PHP.

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Por favor, lee nuestra guía de contribución para más detalles.

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más información.

## 🖥️ Configuración Adicional para Windows

### Configurar el PATH de PHP
Para poder usar los comandos de PHP desde cualquier ubicación:

1. Busca "Variables de entorno" en el menú Inicio
2. Haz clic en "Variables de entorno"
3. En "Variables del sistema", selecciona "Path" y haz clic en "Editar"
4. Agrega la ruta a tu directorio PHP (ej: `C:\php`)

### Solución de Problemas Comunes

- **Error de permisos**: Ejecuta la terminal como administrador
- **Puerto en uso**: Usa `netstat -ano | findstr :8000` para encontrar el proceso usando el puerto
- **Problemas con Composer**: Asegúrate de tener la última versión de Composer instalada

## 📧 Soporte

Si tienes alguna pregunta o encuentras algún problema, por favor [abre un issue](https://github.com/MancillaO/pool_control/issues) en el repositorio.

---

<div align="center">
    Hecho con ❤️ por el equipo de Pool Control
</div>
