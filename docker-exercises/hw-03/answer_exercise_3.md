# a) Installar nginx:1.19.3 por línea de comandos.
![IMAGE MAIN 1](/docker-exercises/hw-03/imatges/1.png)  
# a) Installar nginx con volumen por comandos.
docker run -it --rm -d -p 8080:80 --name homework -v ~/static_content:/usr/share/nginx/html nginx:1.19.3  
# b) Dockerfile:
![IMAGE MAIN 2](/docker-exercises/hw-03/imatges/2.png)  
# b) HTML:
![IMAGE MAIN 3](/docker-exercises/hw-03/imatges/3.png)  
# b) Terminal - Build:
![IMAGE MAIN 4](/docker-exercises/hw-03/imatges/4.png)  
# b) Terminal - Run:
![IMAGE MAIN 5](/docker-exercises/hw-03/imatges/5.png)  
# b) Resultado final:
![IMAGE MAIN 6](/docker-exercises/hw-03/imatges/6.png)  