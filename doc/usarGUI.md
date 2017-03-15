Una buena manera para usar el GUI dentro del docker es (primero ha que tener instalados los x11 en el docker):

<pre>
docker run -it \
    --env="DISPLAY" \
    --env="QT_X11_NO_MITSHM=1" \
    --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" \
    IMAGEN \
    COMANDO
export containerId=$(docker ps -l -q)
</pre>

Saldrá el siguiente error:

<pre>
No protocol specified
</pre>

es normal, no te preocupes.

Mediante la siguien orden se da acceso a las x11 del host:


<pre>
xhost +local:root # for the lazy and reckless
</pre> 

para quitar el acceso cuando se han dejado de usar:

<pre>
xhost -local:root
</pre>

<a href="http://wiki.ros.org/docker/Tutorials/GUI" target="_blank">fuente</a>

