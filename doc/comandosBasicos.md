# Comandos Básicos

<a href="https://docs.docker.com/engine/reference/commandline/docker/" target="_blank" >Referencia de todos los comandos</a>

### docker build
Crea una imagen desde un DockerFile (es conveniente usarlo desde el directorio del dockerfile).

<pre>
docker build [OPTIONS] PATH | URL | -
</pre>

ejemplo:
<pre>
docker build -t ubuntu:base .
</pre>

Algunos flags interesantes:

* -t, --tag : sirve para añadir nombre a la imagen creada

<a href="https://docs.docker.com/engine/reference/commandline/build/" target="_blank" >Referencia</a>

### docker run
Crea una un nuevo contenedor y ejecuta el comando

<pre>
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
</pre>

ejemplo:
<pre>
docker run -ti ubuntu:base bash
</pre>

Algunos flags interesantes:

* -t : abre un tty
* -v : monta un volumen
* --rm: elimina el contendor al final de la ejecución
* --name : asigan nombre al contenedor
* -i : interactivo
* --device: comparte dispositivos con el contendor
* -p : publica un puerto del docker

<a href="https://docs.docker.com/engine/reference/commandline/run/" target="_blank" >Referencia</a>


### docker exec
Ejecuta el comando en el docker

<pre>
docker exec [OPTIONS] CONTAINER COMMAND [ARG...]
</pre>

ejemplo:
<pre>
docker exec -ti ubuntu:base bash
</pre>

Algunos flags interesantes:

* -t : abre un tty
* -i : interactivo

<a href="https://docs.docker.com/engine/reference/commandline/exec/" target="_blank" >Referencia</a>


### docker start
Inicia un contenedor ya creado

<pre>
docker start [OPTIONS] CONTAINER [CONTAINER...]
</pre>

ejemplo:
<pre>
docker start base
</pre>

<a href="https://docs.docker.com/engine/reference/commandline/start/" target="_blank" >Referencia</a>

### docker stop
detiene un contenedor ya iniciado

<pre>
docker stop [OPTIONS] CONTAINER [CONTAINER...]
</pre>

ejemplo:
<pre>
docker stop base
</pre>

<a href="https://docs.docker.com/engine/reference/commandline/stop/" target="_blank" >Referencia</a>

### docker rmi
Elimina una imagen

<pre>
docker rmi [OPTIONS] IMAGE [IMAGE...]
</pre>

ejemplo:
<pre>
docker rmi ubuntu:base
</pre>

<a href="https://docs.docker.com/engine/reference/commandline/rmi/" target="_blank" >Referencia</a>

### docker rm
Elimina un contenedor

<pre>
docker rm [OPTIONS] CONTAINER [CONTAINER...]
</pre>

ejemplo:
<pre>
docker rm base
</pre>

<a href="https://docs.docker.com/engine/reference/commandline/rm/" target="_blank" >Referencia</a>

### docker ps
lista contenedores

<pre>
docker ps [OPTIONS]
</pre>

ejemplo:
<pre>
docker ps -a
</pre>

Algunos flags interesantes:

* -a : muestra todos, incluso los inactivos

<a href="https://docs.docker.com/engine/reference/commandline/ps/" target="_blank" >Referencia</a>


### docker images
lista imagenes

<pre>
docker images [OPTIONS] [REPOSITORY[:TAG]]
</pre>

ejemplo:
<pre>
docker ps -a
</pre>

Algunos flags interesantes:

* -a : muestra todas las imagenes

<a href="https://docs.docker.com/engine/reference/commandline/images/" target="_blank" >Referencia</a>