# Ansible-Test1

Repositorio para probar las funcionalidades de Ansible

<b>-DOCKER:</b>

Lo primero que tenemos que hacer es generar la imagen del servidor ssh lanzado el comando:
<b>docker build -f Dockerfile-ssh -t armijomariano/ssh:${version} .</b>

Para ejecutar un contenedor con la imagen que hemos creado, lanzamos la sentencia:
<b>docker run -d -p ${local_port}:22 --name openssh armijomariano/ssh:${version}</b>

Para ejecutar el script de docker-compose lanzamos el comando:
<b>docker-compose up -d</b>
- SSH server 1 = 192.168.0.2:22 -> localhost:2220
- SSH server 2 = 192.168.0.3:22 -> localhost:2221
- SSH server 3 = 192.168.0.4:22 -> localhost:2222

<b>-ANSIBLE:</b>

Para ejecutar el playbook de ansible, lanzamos la sentencia desde la raiz del proyecto:
<b>ansible-playbook -i ansible/hosts ansible/playbook.yml</b>
