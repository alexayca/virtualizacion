## Vagrant

[Vagrant](https://developer.hashicorp.com/vagrant/downloads)

- Primero instalar un software de virtualizacion como virtualbox.
- Instalamos vagrant (para validar que se instalo correctamente ejecutar en linea de comandos vagrant)
- Para descargar un entorno preconfigurado nos dirigimos a [boxes](https://app.vagrantup.com/boxes/search?provider=virtualbox)
- Seleccionamos uno, para descargarlo en la pestaña new, aparecen los comandos para iniciar el box
- Ejecutamos los comandos en la terminal
    ```
    vagrant init ubuntu/trusty64
    vagrant up
    ```
- Para crear un archivo `Vagrantfile` y establecer el entorno virtual.
- Como alternativa se puede descargar el archivo _.box_ y ejecutar
    ```
    vagrant box add my/box  file:///d:/path/to/name-of-the-box.box
    vagrant init my/box
    vagrant up
    ```
- Loguearse a vagrant ```vagrant ssh```
- Password: vagrant . Para salir exit.
- Para ver el estado ```vagrant status```
- Apagar la maquina ```vagrant halt```
- Apagar y borrar recursos ```vagrant destroy```
