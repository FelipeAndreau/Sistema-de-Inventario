# Sistema-de-Inventario
Sistema de Inventario y Ventas de proposito general desarrollado con PHP y MySQL.

## Modulos
- Productos
- Categorias
- Caja
- Clientes
- Proveedores
- Inventario
- Usuarios

## Instalacion
Para instalar el Sistema Requieres Apache+PHP+MySQL o tener instalado el XAMPP/LAMPP

1. Primero debes descargar este repositorio y colocarlo en tu carpeta htdocs o /var/www/ segun sea el caso.
2. Deberas crear la base de datos llamada inventiolite en tu servidor mysql, las tablas requeridas estan en el archivo schema.sql
3. Deberas modificar el archivo inventio-lite/core/controller/Database.php y agregar los datos de conexion a tu base de datos.
4. Ejecutar el sistema desde http://localhost/inventio-lite/ depende del nombre que le pusiste a la carpeta del proyecto.
5. Los datos de usuario por default son:
    Usuario: admin
    Password: admin
6. DIsfrutar el sistema

---

## 🛠️ Mantenimiento y Mejora del Sistema

Para asegurar la estabilidad y escalabilidad del sistema, se recomienda seguir estas prácticas:

### 1. Mantenimiento Periódico

- **Backups semanales**: Exportar la base de datos desde phpMyAdmin (`Exportar > SQL`) y guardar el archivo.
- **Copias de seguridad del sistema**: Comprimir la carpeta `inventio-lite` y guardarla con la misma frecuencia.
- **Limpieza de tablas**: Revisar tablas como `log`, `ventas` o `caja` para eliminar datos obsoletos si crecen demasiado.
- **Actualización de contraseñas**: Cambiar la contraseña del usuario admin cada cierto tiempo desde la tabla `user`.

---

### 2. Registro y seguimiento de errores

- Usar `try/catch` en archivos PHP críticos (conexiones, inserciones) para capturar errores.
- Crear un archivo `logs/error.log` donde se guarden errores automáticamente.
- Agregar logs de auditoría si el sistema se usa con múltiples usuarios.

---

### 3. Mejora continua

- **Modularización**: separar la lógica en controladores más específicos por entidad (productos, ventas, usuarios).
- **Refactorizar código repetido**: especialmente en archivos PHP con consultas similares.
- **Actualizar a PHP 8.x** si aún se usa una versión antigua, para aprovechar mejoras de rendimiento.
- **Interfaz gráfica**: reemplazar la plantilla por una versión más moderna si se requiere personalización visual.

---

### 4. Seguridad

- Evitar dejar activado `display_errors` en producción.
- Usar `htmlspecialchars()` y `mysqli_real_escape_string()` al mostrar o insertar datos para prevenir inyecciones.
- Agregar validaciones del lado del cliente y servidor para formularios sensibles.

---

### 5. Actualizaciones y despliegue

- Versionar el proyecto usando Git para llevar un historial de cambios.
- Crear una rama `dev` para pruebas y una `main` o `prod` para la versión estable.
- Documentar los cambios en un archivo `CHANGELOG.md`.

---

## 🧪 Recomendación para desarrollo futuro

- Implementar exportación de reportes a PDF o Excel.
- Agregar gráficas con librerías como Chart.js o ApexCharts.
- Incorporar sistema de permisos por rol de usuario.
- Integrar control de stock con alertas de productos bajos.

