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

🔷**docker run** jenkins/jenkins:jdk21

🔷**docker run** redis

🔷**docker run -d** redis

Si usamos -d el contenedor correrá en modo "detached" por lo que no bloqueará la terminal al ejercutarse

--- 

### docker ps 
⭐ Mediante este comando podremos ver los contenedores instalados actualmente corriendo

🔷**docker ps**

---

### docker stop container_name/id
⭐ Este comando parará el contenedor que esté corriendo, si no asignamos un nombre se hará automáticamente, podemos ver los nombres asignados a cada contenedor con *docker ps*.

🔷**docker stop** vibran_cohen

---

### docker start container_name/id
⭐ Este comando iniciará el contenedor que esté corriendo, si no asignamos un nombre se hará automáticamente, podemos ver los nombres asignados a cada contenedor con *docker ps*.

🔷**docker start** vibran_cohen

---