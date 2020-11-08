# CMD VS ENV
## ENV:
La variable ENV nos permite darle un valor ("setear") a las variables de entorno dentro de nuestro contenedor.  
Utiliza **key** = **value** **:
### Ejemplo:
* ENV nginx_vhost /etc/nginx/sites-available/default 
* ENV php_conf /etc/php/7.4/fpm/php.ini 
* ENV nginx_conf /etc/nginx/nginx.conf 
* ENV supervisor_conf /etc/supervisor/supervisord.conf 

Esto nos facilitara a la hora de interactuar con la consola del contenedor y a la hora de lanzar ejecuciones.

## CMD:
Nos permite lanzar comandos dentro del cmd de la máquina. Ejecutar instruciones como si estuviésemos en el terminal de la máquina.
Se utiliza normalmente al final del Dockerfile para lanzar la ejecución después de haberlo configurado.
### Ejemplo:
CMD [“executable”,” param1”,” param2”]: CMD [“addNumbers.py”,”2”,”4”] 
En este caso nos permite ejecutar el fichero addNumbers pasandole los parámetros 2 y 4.

### Diferencia:
ENV nos permite especificarles las variables de entorno dentro de la maquina mientras que CMD nos permite lanzar ejecuciones/comandos como si estuviéramos dentro del CMD del contenedor.
