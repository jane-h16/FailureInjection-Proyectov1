# FailureInjection-Proyectov1
### Proyecto Rancher-Wordpress 
Computación Tolerante a Fallas 

Nombre: Huerta Bustamante Janette Guadalupe

### ¿En qué consiste el proyecto? 
Rancher admite varios motores de orquestación para sus entornos administrados, incluidos Kubernetes, usaremos Rancher y Docker para crear un entorno de WordPress  disponible y escalable, con la ayuda del Clúster creado en K3S. El servicio de WordPress tiene dos enlaces externos a la pila e inicia el contenedor como un contenedor privilegiado para que pueda montar el volumen Storage Class y su dependencia con MariaDB.

Esto simplifica a la creación de entornos altamente disponibles, escalables y distribuibles listos para su uso en producción.

### ¿Qué finalidad tiene el proyecto?
Al implementar una instalación de WordPress con servicios para dar inicio de cero al almacenamiento, base de datos, aplicación web y Load Balancers.
También su uso generá escenarios comunes de error/degradación de producción y demostrar que es tolerante a fallas, ya que los usuarios no experimentarán ninguna interrupción del servicio gracias a Kubernetes.

### :heavy_check_mark: Tecnologías Aplicadas
- Docker
- Kubernetes
- WordPress
- K3S
- Rancher
- GitHub

### Instalación de Docker 
1. Actualiza tu sistema
Ejecuta los siguientes dos comandos:
```
sudo apt update
sudo apt upgrade
```

2. Agrega los repositorios de Docker
Ahora tienes que agregar los repositorios de Docker. Esto facilitará mucho el proceso de instalación y al mismo tiempo podrás utilizar el método de instalación oficialmente compatible.

Primero, agrega la clave GPG, ingresando el siguiente comando en la línea de comando:
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
3. A continuación, agrega el repositorio:
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```
4. Después de eso, actualiza la información del repositorio:
```
sudo apt update
```
Puedes asegurarte de estar instalando desde el repositorio de Docker en lugar del repositorio predeterminado de Ubuntu con este comando:
```
apt-cache policy docker-ce
```
Una salida correcta se verá como la siguiente con diferentes números de versión:
docker-ce:
   Installed: (none)
   Candidate: 16.04.1~ce~4-0~ubuntu
   Version table:
       16.04.1~ce~4-0~ubuntu 500
            500 https://download.docker.com/linux/ubuntubionic/stableamd64packages
Como puedes ver, docker-ce no está instalado, por lo que podemos pasar al siguiente paso.

5. Instala Docker en Linux
```
sudo apt install docker-ce
```
6. Comprueba el estado de Docker
Una vez que se completa la instalación, es buena idea verificar el estado del servicio:
```
sudo systemctl status docker
```

Una vez que Docker está instalado, todo lo que tienes que hacer es usar la imagen de prueba para verificar que todo funcione como debería. Puedes hacer esto con el siguiente comando:
```
sudo docker run hello-world
```

### Instalación de Rancher 

La instalación de Rancher es sencilla, lo primero que nos dice que tengamos una maquina Linux con al menos 4GB de memoria y con Docker instalado.
Para instalarlo ejecutamos en la maquina el siguiente comando:

```
$ sudo docker run -d –restart=unless-stopped \
 -p 80:80 -p 443:443 rancher/rancher
```
