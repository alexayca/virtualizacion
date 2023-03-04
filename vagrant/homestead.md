# homestead

[homestead](https://github.com/laravel/homestead)

Utilizaremos la imagen de Laravel Homestead siguiendo los pasos que aquí se describen: [v 5.7](https://laravel.com/docs/5.7/homestead). Las imágenes de Vagrant se llaman box o cajas, Homestead es una de ellas.
- ```vagrant box add laravel/homestead``` para instalar la imagen de homestead (sobre el motor de la maquina virtual virtualbox)
- clonamos el proyecto ```git clone https://github.com/laravel/homestead.git ~/Homestead``` que se instalara en la carpeta home del usuario.
- Cuando inicializamos Homestead, lo que hacemos es crear un nuevo archivo de configuración ___Homestead.yaml___. Para inicializar el proyecto ```bash init.sh``` en linux o en windows ```init.bat``` con CMD
- Editamos el archivo ___Homestead.yaml___ para añadir DDBB y proyectos a la misma maquina:
    - la __IP__ que no es localhost
    - __folders:__ ubicación donde esta la carpeta del proyecto en el host (WSL) [__map: /mnt/c/www__], a la maquina virtual (guest) [__to: /home/vagrant/code__].
    - __sites:__ permite agregar diferentes proyectos, por cada proyecto se agrega __- map: proyecto.test__ y __to: /home/vagrant/code/proyecto/public__, que es equivalente al de __folders:__ más la dirección publica del proyecto (index donde inicia el proyecto).
    - __databases:__ para añadir ls DB __- nombreBaseDatos__ 
- Una vez configurado, esta lista para levantarse con ```vagrant up``` desde la carpeta donde descargamos la configuracion la maquina virtual.
- Se creara la máquina virtual vagrant si no existe; si existe se reiniciará la máquina existente.
- Se ejecutará también el aprovisionamiento (configurar e instalar lo que se necesite).  Si se modifica se puede actualizar con ```vagrant reload --provision``` o ```vagrant up --provision```
- Para validar que funciona la maquina virtual, en el navegador visitaremos la dirección ip que aparecia en el archivo ___Homestead.yaml___ o el host virtual si lo creamos. 
