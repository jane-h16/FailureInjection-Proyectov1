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

