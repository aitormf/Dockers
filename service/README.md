# Hacer que el servicio de docker escuche petiocones de otros PCs

* Cambiar "port" por el pùerto deseado en la siguiente linea del fichero "docker.service":

<pre>
ExecStart=/usr/bin/dockerd -H fd:// -H tcp://0.0.0.0:port
</pre>

* copiar los ficheros a "/etc/systemd/system" y reiniciar el servicio:

<pre>
sudo cp docker.* /etc/systemd/system
sudo systemctl daemon-reload
sudo systemctl restart docker
</pre>

* comprobar el funcionamiento:

<pre>
systemctl status docker.service
</pre> 


