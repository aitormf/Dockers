# Primeros Pasos

Lo primero que hay que hacer es instalar Docker.

## Instalacion de Docker

sigue las instrucciones de <a href="https://www.docker.com/community-edition" target="_blank" >este enlace</a>

## Añadir usuario al grupo Docker

Añadimos nuestro usuario al grupo docker
<pre>
sudo gpasswd -a ${USER} docker
</pre>

Actualizamos el grupo

<pre>
sudo newgrp docker
</pre>


## Algunos tutoriales para aprender lo básico:

* <a href="https://www.adictosaltrabajo.com/tutoriales/docker-for-dummies/" target="_blank" >Docker para dummies</a>
* <a href="https://docs.docker.com/engine/getstarted/" target="_blank" >Get started with Docker</a>
* <a href="https://docs.docker.com/engine/reference/builder/" target="_blank" >DockerFile Reference</a>
