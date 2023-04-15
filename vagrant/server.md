Considere que al cambiar la versión de php como se indica, solo se esta actualizando la versón que utiliza la linea de comandos, y no la que ejecuta el servidor web.


# nginx
- Configuración del dominio de virtualhost: **/etc/nginx/sites-available/**

- Se tiene que cambiar la línea donde se indica el motor de ejecución de PHP. 
**fastcgi_pass unix:/var/run/php/php8.0-fpm.sock;**

- Para verificar si no hay errores en la configuración: 
``` sudo nginx -t ```

- Reiniciar nginx:
``` sudo systemctl reload nginx.service ```

Para ver el status de ejecución:
``` sudo systemctl status nginx ```



# apache2
Configuración del dominio de virtualhost: **/etc/apache2/sites-available/**

[activar modulos en apache](https://www.swhosting.com/es/comunidad/manual/como-activar-y-desactivar-modulos-en-apache)

Para ver el status de ejecución:
``` sudo systemctl status apache2 ```

