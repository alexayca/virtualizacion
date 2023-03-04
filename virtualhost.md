# Virtual Host

[que es?](https://linube.com/ayuda/articulo/267/que-es-un-virtualhost)
[en apache](https://www.desarrollolibre.net/blog/apache/que-son-y-como-emplear-los-virtualhost-en-apache)

El archivo host sirve para indicarle a nuestra computadora que cierta _url_ está relacionada con cierta _IP_. Se debe modificar este archivo para que al escribir cierta _url_, el explorador nos redirija a una _ip_ especifica.

El archivo hosts se encuentra respectivamente en:
- ```/etc/host```
- ```C:\Windows\System32\drivers\etc\hosts```

Aqui editamos el archivo indicando la dirección IP seguida del host.

```127.0.0.1   dominio.test```


## homestead
En el caso de _homestead_ se usa la _IP_ declarada en el archivo __Homestead.yaml__ en la linea `ip: "nnn.nnn.nnn.nnn"` y la _url_ será el que inidiquemos en `sites: - map: dominio.test`

