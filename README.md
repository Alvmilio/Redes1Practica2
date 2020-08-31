# Practica 2 -  Redes de Computadoras 1

## Topologia a realizar 🖇️
- Imagen
    ![s](/Images/topology.jpg)


## Configuracion de la Topologia 🔧

- Agregar imagen del Router dentro de GNS3
    - Nos dirigimos al apartado de Edit, luego a preferencias y finalmente donde dice Dynamips - IOS Routers procedemos a presionar New
    - Si queremos importar una imagen que no fue utilizada previamente seleccionamos New Image y luego le damos a Browse para seleccionar el archivo .image
    - De lo contrario pues lo seleccionamos del dropdown menu que nos aparece en Existing image.
    - Damos click en next
    - Ingresamos Nombre, Platform y chassis. Le damos click a next
    - Si deseamos establecer un valor de RAM es especifico pues lo ingresamos, de lo contrario lo dejamos como esta y damos click en next
    - Escogemos los adaptadore de red que debe tener el router, luego le damos a next
    - Le damos otra vez a next
    - Y finalmente Finish
- Agregamos la maquina virtual dentro de los dispositivos de GNS3
    - Nos dirigimos al apartado de Edit, luego a preferencias y finalmente donde dice VMWare VM's y procedemos a presionar New
    - Seleccionamos la maquina (debe estar previamente creada dentro de VMware) a importar
    - Presionamos Finish
- Seleccionar los elementos que utilizaremos en la topologia
    - 1 router c3725
    - 2 switch 
    - 3 VPC
    - 1 Instancia de maquina virtual VMware 
- Procedemos a realizar las conexiones necesarias entre dispositivos
- Para una mejor presentacion agregamos Labels en cada dispositivo segun corresponda
- Configuramos el router
    -  Click derecho en el router y Start
    -  Accedemos a la consola del router
    -  Ingresamos los comandos listados a continuacion
    ![s](/Images/routerConf2.png)
- Configuramos las computadoras
    - Encendemos la maquina que configuraremos
    - Accedemos la consola e ingresamos los siguientes comandos
    
    ![s](/Images/pcConfig2.jpg)
- Configuramos la maquina virtual de VMware
    - Encedemos la maquina desde GNS3
    - Nos dirigimos a panel de control
    - Seleccionamos NetWork
    - Ingresamos los datos mostrados a continuacion
    ![s](/Images/TLNetwork2.jpg)
    - El resto de datos se llenaran de manera automatica al ingrgesa la IP
    
## Realizamos las pruebas necesarias 🚀
- Ingresamos a la maquina 1
    - Hacemos ping al resto de maquinas
    ![s](/Images/PC1Ping.png)
- Ingresamos a la maquina 2
    - Hacemos ping al resto de maquinas
    ![s](/Images/PC2Ping.png)
- Ingresamos a la maquina 3
    - Hacemos ping al resto de maquinas
    ![s](/Images/PC3Ping.png)
- Ingresamos a la maquina virtual de VMware
    - Hacemos ping al resto de maquinas
    ![s](/Images/TLPing.png)
## Captura de paquetes con WireShark 
    ![s](/Images/WireShark.jpg)
## Glosario 📖   
- Router
    - Dispositivo que permite interconectar computadoras que funcionan dentro de una misma red. Este ademas, se encarga de asignar las direcciones IP
- Switch
    - Dispositivo encargado de distribuir los datos recibidos a cada maquina destino dentro de la configuracion de la red
- Topologia
    - Mapa logico diseñado para identificar de una mejor manera una red.
- Interface
    - Tarjeta o circuito instalado en un dispositivo para permitir que este se conecte a una LAN
- Fast Ethernet
    - Nombre del estandar IEEE para las redes ethernet que alcanzan los 100 Mbps
- DNS
    - Acronimo de Domain Name System, es un sistema de nomenclatura utilizado para dispositivos conectados a alguna red. Su funcion es traducir 
    nombres entendibles por personas a identificadores binarios asociados a la red.
- Gateway
    - Puerta de enlace, su proposito es traducir la informacion del protocolo utilizado en una red inicial, al protocolo usado en la red destino
- Telnet
    - Protocolo de red que permite acceder a otra maquina para manejarla remotamente.
- SSH
    - Secure Shell, protocolo para acceso remoto a un servidor por medio de un canal seguro. Su principal diferencia con telnet es la seguridad, ya que con SSH la informacion a enviar es criptada mientras que con telnet esta se envia expuesta.
- DHCP
    - Protocolo de red encargado de asignar direcciones IP de manera dinamica. Cuenta con una lista de direcciones IP que va asignando a los dispositivos conforme van quedando libres.