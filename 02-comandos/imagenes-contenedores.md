# Comandos básicos: **imágenes**

### docker pull image_name
⭐ Mediante este comando instalaremos una imagen en su última versión

🔷**docker pull** jenkins/jenkins:jdk21

🔷**docker pull** redis

---

### docker images 
⭐ Mediante este comando podremos ver las imágenes que tenemos instaladas

🔷**docker images**

---

# Comandos básicos: **contenedores**

### docker run image_name
⭐ Con este comando haremos correr una imagen en un contenedor, de este modo podremos ponerla en uso. Para detener la ejecución usaremos *Cntrl + C*.

🔷**docker run** redis

🔷**docker run** jenkins

🔷**docker run -d** redis

Si usamos -d el contenedor correrá en modo "detached" por lo que no bloqueará la terminal al ejercutarse

🔷**docker run -d** redis:4.0

Si usamos :4.0 le estaremos diciendo que instale la versión 4.0 de redis

--- 

### docker run -pMI_PUERTO:PUERTO_DE_LA_APP container_name/id
⭐ Con este comando remapearemos el puerto de la aplicación para que escuche en nuestro ordenador local.

🔷**docker run -p6000:6379** redis

---

### docker run --name NOMBRE_PERSONALIZADO imagen
⭐ Con este comando podemos seleccionar el nombre de la imagen

🔷**docker run --name redis-old** redis

🔷**docker run -d -p6000:6379 --name redis-old** redis

Podemos enlazar el modo detached y el remapeo de puertos

---

### docker ps 
⭐ Mediante este comando podremos ver los contenedores instalados actualmente corriendo

🔷**docker ps**

🔷**docker ps -a**

Si usamos -a podremos ver los contenedores que están activos y parados al mismo tiempo

---

### docker stop container_name/id
⭐ Este comando parará el contenedor que esté corriendo, si no asignamos un nombre se hará automáticamente, podemos ver los nombres asignados a cada contenedor con *docker ps*.

🔷**docker stop** vibran_cohen

---

### docker start container_name/id
⭐ Este comando iniciará el contenedor seleccionado, si no asignamos un nombre se hará automáticamente, podemos ver los nombres asignados a cada contenedor con *docker ps*.

🔷**docker start** vibran_cohen

---

### docker logs container_name/id
⭐ Con este comando podemos ver los logs del contenedor que iniciamos para permitir el debugeo

🔷**docker logs** vibran_cohen

---

### docker exec -it container_name/id /bin/bash
⭐ Con este comando podremos navegar internamente en el contenedor en modo bash, de este modo podremos ver lo que contiene el contenedor y usar comandos como ls, mkdir, etc... Para salir de la terminal bash: *exit*

🔷**docker exect -it** vibran_cohen **/bin/bash**