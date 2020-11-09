# ENTRYPOINT VS CMD 🖥⚔️ ️

![ENV VS ENTRYPOINT](/docker-exercises/hw-05/imatges/CMDvsENV.PNG)  

## ENTRYPOINT:
La variable ENV nos permite darle un valor ("setear") a las variables de entorno dentro de nuestro contenedor. Las variables de entorno se utilizan para reducir un path (ruta del explorador de ficheros) en una sola palabra.  
Utilizando **&lt;key>** … **&lt;value>**:
### Ejemplo:
* **ENTRYPOINT** nginx_vhost /etc/nginx/sites-available/default 
* **ENTRYPOINT** php_conf /etc/php/7.4/fpm/php.ini 
* **ENTRYPOINT** nginx_conf /etc/nginx/nginx.conf 
* **ENTRYPOINT** supervisor_conf /etc/supervisor/supervisord.conf 

Esto nos facilitara a la hora de interactuar con la consola del contenedor y cuando queramos lanzar ejecuciones.

## CMD:
Nos permite lanzar comandos dentro del cmd (Símbolo del sistema) de la máquina. Ejecutar instruciones como si estuviésemos en el terminal de la máquina.
Se utiliza normalmente al final del Dockerfile para lanzar la ejecución después de haber configurado todo el contenedor, para así ejecutar la aplicacion/servicio.

### Ejemplo:
* **CMD** [“executable”,” param1”,” param2”]
* **CMD** [“addNumbers.py”,”2”,”4”]


En este caso nos permite ejecutar el fichero **addNumbers** pasandole los parámetros **2** y **4**.

### Diferencia:
* **ENV** nos permite especificarles las variables de entorno dentro de la maquina para facilitar las ejecuciones mientras que **CMD** nos permite lanzar ejecuciones/comandos como si estuviéramos dentro del terminal del contenedor. 

## Aclaraciones
* Normalmente se llama a variables de entorno dentro del CMD (Primero ENV despues CMD).