# labs-docker-dev

## Imagen ubuntu 
 
<b>sebas@guerrero:~$ `sudo docker pull ubuntu` </b><br> 
Using default tag: latest </b>
latest: Pulling from library/ubuntu </b>
9c704ecd0c69: Pull complete </b>
Digest: sha256:2e863c44b718727c860746568e1d54afd13b2fa71b160f5cd9058fc436217b30 </b>
Status: Downloaded newer image for ubuntu:latest </b>
docker.io/library/ubuntu:latest 

## Imagen Python

<b>sebas@guerrero:~/Escritorio$ `sudo docker pull python:3.9`</b><br> 

sebas@guerrero:~$ sudo docker pull python:3.9 </b>
3.9: Pulling from library/python </b>
ca4e5d672725: Pull complete  </b>
30b93c12a9c9: Pull complete  </b>
10d643a5fa82: Pull complete  </b>
d6dc1019d793: Pull complete  </b>
c7d45ab0573c: Pull complete  </b>
564d1c451ea7: Pull complete  </b>
ddfb50ba1977: Pull complete  </b>
91b87d81d4c8: Pull complete  </b>
Digest: sha256:65438c2e26dbf9f5db4b5553e332747fa20722c1b7c7ccc6f8480396ff4186db </b>
Status: Downloaded newer image for python:3.9 </b>
docker.io/library/python:3.9 </b>


##  Ejecuta un contenedor de Ubuntu en modo interactivo

<b>sebas@guerrero:~$ `sudo docker run -it ubuntu bash` </b></br> 

root@956a6c860ffa:/# exit </br>
exit

## Ejecutar un servidor web Apache en segundo plano, mapeando el puerto 8000 del host al puerto 80 del contenedor:

<b>sebas@guerrero:~$ `sudo docker run -d -p 9000 httpd` </b></br>

af354589ca5772f5cd525d21e8805724662dc636d358930b66d16b0138b34048

## Removing containers (Eliminar contenedores)

### Usar docker ps -a para ver todos los contenedores (incluyendo los detenidos).

<b>sebas@guerrero:~$ `sudo docker ps -a`</b></br>

CONTAINER ID   IMAGE     COMMAND              CREATED         STATUS                       PORTS                                                 NAMES
af354589ca57   httpd     "httpd-foreground"   2 minutes ago   Up 2 minutes                 80/tcp, 0.0.0.0:32768->9000/tcp, :::32768->9000/tcp   gallant_cray
af7c38fa72a7   httpd     "httpd-foreground"   2 minutes ago   Exited (0) 2 minutes ago                                                           hopeful_curran
c9c0866af42b   httpd     "httpd-foreground"   3 minutes ago   Created                                                                            inspiring_wozniak
01d356fad082   httpd     "httpd-foreground"   3 minutes ago   Created                                                                            nifty_engelbart
956a6c860ffa   ubuntu    "bash"               5 minutes ago   Exited (0) 4 minutes ago                                                           magical_poincare
90e3c54f6e42   ubuntu    "bash"               7 minutes ago   Exited (130) 5 minutes ago                                                         affectionate_heyrovsky

### Usar docker rm seguido del ID o nombre del contenedor.

<b> sebas@guerrero:~$ `sudo docker rm 956a6c860ffa`</b><br>
956a6c860ffa

### sebas@guerrero:~$ docker container prune

<b> sebas@guerrero:~$ `docker container prune` </b><br>
WARNING! This will remove all stopped containers. </br>
Are you sure you want to continue? [y/N] y </br>
Deleted Containers: </br>
af7c38fa72a721c80b30ee88e7a8148688bb98c149f75bce3f2f99df39dd3fea </br>
c9c0866af42b6cfdfa66f505474dcde44d352b7bf7b37d670743e1462c01f7a3 </br>
01d356fad0821cb71446d2f4ad6a4a2b132a3f57027528e5a3bb5bf08169f66f </br>
90e3c54f6e428e8a2ea96dee74c7f28eb033fbb98cb769fe2530c20a5f138c56 </br>
<br/>
Total reclaimed space: 7B </br>



