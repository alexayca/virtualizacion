# Change PHP version


## Laravel homestead
[stackoverflow](https://stackoverflow.com/questions/47849825/change-laravel-homestead-v7-0-1-with-php-7-2-to--7-1)

### Linea de comandos
- Para cambiar la versión de php ejecuta: 
``` sudo update-alternatives --config php ``` 
y selecciona la versión deseada.

- En las nuevas versiones de homestead se puede usar: 
``` php80 ```
donde representa *php 8.0* 

- Ejecutar los comandos en conjunto con la versión ``` php8.0 artisan ```

- O bien agregar el tag **php: "8.0"** en el archivo *yaml* de homestead.
```yaml
sites:
    - map: homestead.test
      to: /home/vagrant/Code/homestead/public
      php: "8.0"
```
