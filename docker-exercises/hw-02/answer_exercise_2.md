# ADD VS COPY 🖥⚔️ ️

* Los dos utilizan la misma lógica mover un fichero conservandolo en los dos lados (ADD/COPY) **&lt;src>** … **&lt;dest>**

## COPY:
Toma un **SRC** y un **destino**. Sólo te permite **copiar** en un **archivo** o **directorio local** de tu **host** (la máquina sobre la que se ejecuta la imagen del Docker) dentro del contenedor.

### Ejemplo:
* **Host** --> **Docker** : **COPY** /source/file/path  /destination/path


## ADD:
Te permite hacer lo mismo que el COPY pero también soporta otros tipos de fuentes **&lt;src>**. 
Puedes usar de fuente :
* Ficheros **archivo** o **directorio local** (igual que COPY).
* Una **URL** en ves de un fichero local/directory. 
* Ficheros Tar como identity, gzip, bzip2 or xz.


### Ejemplo:
* **Host -> Docker**. **Example: ADD** /source/file/path  /destination/path
* **URL -> Docker**. **Example: ADD** http://source.file/url  /destination/path
* **Tar File (identity, gzip, bzip2 or xz) -> Docker**. **Example: ADD** source.file.tar.gz /temp


## Resumen
* **COPY** Copia un archivo/directorio de su host a su imagen.

* **ADD** Copia un archivo/directorio de su host a su imagen, pero también puede obtener URLs , extraer archivos TAR, etc...