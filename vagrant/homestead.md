# homestead

[github homestead](https://github.com/laravel/homestead)

## Configuración en windows
Utilizaremos la imagen de Laravel Homestead siguiendo los pasos que aquí se describen: [v 5.7](https://laravel.com/docs/5.7/homestead). Las imágenes de Vagrant se llaman box o cajas, Homestead es una de ellas.

- ```vagrant box add laravel/homestead``` para instalar la imagen de homestead (sobre el motor de la maquina virtual virtualbox)
- clonamos el proyecto ```git clone https://github.com/laravel/homestead.git C:\path\Homestead``` que se instalara en la carpeta home del usuario.
- Cuando inicializamos Homestead, lo que hacemos es crear un nuevo archivo de configuración ___Homestead.yaml___. Para inicializar el proyecto ```bash init.sh``` en linux o en windows ```init.bat``` con CMD
- Editamos el archivo ___Homestead.yaml___ para añadir DDBB y proyectos a la misma maquina:
    - la `ip:` que no es localhost
    - `folders:` ubicación donde esta la carpeta del proyecto en el host ` map: - map: C:\path\ ` (_C:\path\proyecto\public_), a la maquina virtual (guest) `to: /home/vagrant/code`.
    - `sites:` permite agregar diferentes proyectos, por cada proyecto se agrega `- map: proyecto.test` y `to: /home/vagrant/code/proyecto/public`, que es equivalente al de `folders:` más la dirección publica del proyecto (index donde inicia el proyecto).
    - `databases:` para añadir ls DB `- nombreBaseDatos` 
- Una vez configurado, esta lista para levantarse con ```vagrant up``` desde la carpeta donde descargamos la configuracion la maquina virtual.
- Se creara la máquina virtual vagrant si no existe; si existe se reiniciará la máquina existente.
- Se ejecutará también el aprovisionamiento (configurar e instalar lo que se necesite).  Si se modifica se puede actualizar con ```vagrant reload --provision``` o ```vagrant up --provision```
- Para validar que funciona la maquina virtual, en el navegador visitaremos la dirección ip que aparecia en el archivo ___Homestead.yaml___ o el host virtual si lo creamos. 



## Virtualbox

Carpetas compartidas (Carpetas de la maquina virtual con archivo .yaml)
```
- home_vagrant_code
    folders: to: /home/vagrant/code     \\?\C:\tmp
- vagrant
    \\?\C:\tmp\vagrant_project\homestead\Homestead
```

Archivo ___Homestead.yaml___
```
folders:
    - map: C:\tmp\
      to: /home/vagrant/code

sites:
    - map: constancias.test
      to: /home/vagrant/code/ConstanciasDEJC/public
```

