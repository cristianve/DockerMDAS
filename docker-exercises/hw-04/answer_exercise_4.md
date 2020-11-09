# HEALTHCHECK 🖥👨‍⚕️ ️

El healthcheck deberá parametrizarse con la siguiente configuración: 

• La prueba se realizará cada 45 segundos:

    HEALTHCHECK --interval=45s

• Por cada prueba realizada, se esperará que la aplicación responda en menos de 5 segundos. Si tras 5 segundos no se obtiene respuesta, se considera que la prueba habrá fallado.

    --timeout=5s

• Ajustar el tiempo de espera de la primera prueba (Ejemplo: Si la aplicación del contenedor tarda en iniciarse 10s, configurar el parámetro a 15s).
-- start-period=15s
• El número de reintentos será 2. Si fallan dos pruebas consecutivas, el contenedor deberá cambiar al estado “unhealthy”).

    --retries=2

# Creacion de script sh
Nos dice si la pagina esta alive "0" o no "1":  

    #!/bin/bash  
    curl -f -s -I "localhost:8080" &>/dev/null && echo 0 || echo 1
    exit 0;

# Healthcheck Dockerfile:

    HEALTHCHECK --interval=45s --timeout=5s --start-period=15s --retries=2 CMD ["sh","/healthcheck.sh"]
    
# Resultado

![HEALTHCHECK](/docker-exercises/hw-04/imatges/resultado.png)  

# Opción optimizada Healthcheck :

    HEALTHCHECK --interval=45s --timeout=5s --start-period=15s --retries=2 CMD curl -f http://localhost:80 || exit 1
    
