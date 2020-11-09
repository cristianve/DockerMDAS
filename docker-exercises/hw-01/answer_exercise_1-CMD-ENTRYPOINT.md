# ENTRYPOINT VS CMD 🖥⚔️ ️

![ENV VS ENTRYPOINT](/docker-exercises/hw-01/imatges/CMDvsENV.PNG)  

## ENTRYPOINT:
La instrucción ENTRYPOINT le permite configurar un contenedor que se ejecutará como un ejecutable. 

### Ejemplo 2 formas de usar ENTRYPOINT:
* **ENTRYPOINT** ["executable", "param1", "param2"] (exec form, preferred)
* **ENTRYPOINT** command param1 param2 (shell form) 

El ENTRYPOINT es el programa que se ejecutará, y el valor pasado al contenedor se añadirá al mismo.


## CMD:
El propósito principal de un CMD es proporcionar argumentos para un contenedor de ejecución. Nos permite lanzar comandos dentro del CMD (Símbolo del sistema) del contenedor como si estuviesemos dentro de esta.

### Ejemplo:
* **CMD** [“executable”,” param1”,” param2”]
* **CMD** [“addNumbers.py”,”2”,”4”]

En este caso nos permite ejecutar el fichero **addNumbers** pasandole los parámetros **2** y **4**.

### Diferencia:
* ENTRYPOINT define el ejecutable invocado cuando se inicia el contenedor (para el comando)

* CMD especifica los argumentos que se pasan al ENTRYPOINT (para los argumentos)

### Tips
* El ENTRYPOINT puede ser anulado especificando un indicador --entrypoint, seguido del nuevo punto de entrada que se desea utilizar.* 