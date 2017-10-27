## DNS Windows   Server ##

Comenzamos creando en *Windows 2012 Server* una **Zona de Búsqueda Directa e Inversa**, para servir las resoluciones de IP´s a nombres de dominio y viceversa, despues de instalar el servidor DNS en *Herramientas*:

![img](./images/1.png)

Aqui es donde indicamos que queremos crear ambas zonas de búsqueda:

![img](./images/2.png)

![img](./images/3.png)

![img](./images/5.png)

Le asignamos un nombre para tenerla identificada, en éste caso le ponemos la dirección de red que utilizamos:

![img](./images/7.png)

![img](./images/8.png)

![img](./images/9.png)

![img](./images/10.png)

![img](./images/12.png)

![img](./images/13.png)

Aquí indicamos donde enviaría las consultas, y indicamos, por ejemplo, los DNS de *Google*

![img](./images/14.png)

![img](./images/15.png)

Aquí se puede comprobar la correcta conexión:

![img](./images/comprobacion_dns_cache_y_maestro.png)

----

Vamos a crear en la zona de búsqueda directa un registro llamado **servicios** donde añadiremos varias entradas:

* Un alias para tu servidor denominado server.
* Una impresora con IP fija denominada printer (no hace falta alias).
* Un servidor de correo (ficticio) denominado correo, asociado a una dirección en tu servidor.
* Crear una subzona denominada servicios (dominio nuevo) y agregar a ésta un servidor ftp (asociado a la misma IP del servidor), una impresora nueva (con una IP fija) y el equipo del administrador del sistema (también con IP fija).

Se añaden de la misma manera, difiere los nombre y direcciones IP´s:

![img](./images/5_zona_servicios.png)

Una vez realizados todos los registros comprobamos:

![img](./images/7comprobacionservicios.png)
-----

Creamos los enlaces CNAME Y MX:

Seguimos con la validación de un cliente y la comprobación de éste haciendo uso del comando `nslookup`:

![img](./images/99.png)

![img](./images/9_comprobacion.png)
