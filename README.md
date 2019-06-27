# Ansible-Test1

Repositorio para probar las funcionalidades de Ansible

Lo primero que tenemos que hacer es generar la imagen del servidor ssh lanzado el comando:
<b>docker build -f Dockerfile-ssh -t armijomariano/ssh:${version} .</b>

Para ejecutar un contenedor con la imagen que hemos creado, lanzamos la sentencia:
<b>docker run -d -p ${local_port}:22 --name openssh armijomariano/ssh:${version}</b>
