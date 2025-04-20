# Repositorios remotos y servidores
Para poder colaborar en cualquier proyecto Git, necesitas saber cómo gestionar repositorios remotos. Los repositorios remotos son versiones de tu proyecto que están hospedadas en Internet o en cualquier otra red. Puedes tener varios de ellos, y en cada uno tendrás generalmente permisos de solo lectura o de lectura y escritura. Colaborar con otras personas implica gestionar estos repositorios remotos enviando y trayendo datos de ellos cada vez que necesites compartir tu trabajo. Gestionar repositorios remotos incluye saber cómo añadir un repositorio remoto, eliminar los remotos que ya no son válidos, gestionar varias ramas remotas, definir si deben rastrearse o no y más. En esta sección, trataremos algunas de estas habilidades de gestión de remotos.

# Ver Tus Remotos
En Git, para ver los remotos que tienes configurados, debes ejecutar el comando git remote. Mostrará los nombres de cada uno de los remotos que tienes especificados. Si has clonado tu repositorio, deberías ver al menos origin (origen, en inglés) - este es el nombre que por defecto Git le da al servidor del que has clonado:

$ git clone https://github.com/schacon/ticgit
Cloning into 'ticgit'...
remote: Reusing existing pack: 1857, done.
remote: Total 1857 (delta 0), reused 0 (delta 0)
Receiving objects: 100% (1857/1857), 374.35 KiB | 268.00 KiB/s, done.
Resolving deltas: 100% (772/772), done.
Checking connectivity... done.
$ cd ticgit
$ git remote
origin
También puedes pasar la opción -v, la cual muestra las URLs que Git ha asociado al nombre y que serán usadas al leer y escribir en ese remoto:

$ git remote -v
origin	https://github.com/schacon/ticgit (fetch)
origin	https://github.com/schacon/ticgit (push)
Se puede tener un repositorio con más de un remoto, por ejemplo, para trabajar con distintos colaboradores.

# Añadir Repositorios Remotos
Para añadir en git un remoto nuevo y asociarlo a un nombre que puedas referenciar fácilmente, ejecuta git remote add [nombre] [url]:

$ git remote
origin
$ git remote add pb https://github.com/paulboone/ticgit
$ git remote -v
origin	https://github.com/schacon/ticgit (fetch)
origin	https://github.com/schacon/ticgit (push)
pb	https://github.com/paulboone/ticgit (fetch)
pb	https://github.com/paulboone/ticgit (push)

## Entrega
Responde: 

1-Qué es un repositorio remoto, permisos y su importancia en la colaboración de proyectos

Un **repositorio remoto** es una versión del repositorio de Git que se aloja en un servidor (como GitHub, BitBucket o GitLab), accesible a través de Internet o una red. Los permisos asociados pueden ser de **solo lectura** o de **lectura y escritura**, lo cual determina si puedes únicamente ver el contenido o también modificarlo.

Su importancia radica en que permite la **colaboración entre múltiples desarrolladores**, centralizando los cambios, facilitando la integración del código, el seguimiento de versiones y el trabajo en equipo distribuido.

---

2-origin. Qué es.

`origin` es el **nombre por defecto** que Git asigna al repositorio remoto desde el que se clona un proyecto. Representa la URL original y facilita los comandos de sincronización (`git fetch`, `git push`, `git pull`) sin necesidad de especificar la dirección completa del repositorio.

---

3-Servidor BitBucket. Date de alta en BitBucket y crea un repositorio Hola Mundo. Manda un pantallazo con el  historial de commits realizados (identificador SHA-1)

- Crear una cuenta en [BitBucket](https://bitbucket.org/).
- Crear un repositorio llamado **Hola Mundo**.
- Realizar al menos un commit.
- Adjuntar aquí un pantallazo con el historial de commits realizados, mostrando el **identificador SHA-1**.

---

4-Sube a tu servidor BitBucket un segundo repositorio: el de la última práctica Git. Haciendo una copia en remoto . PARA ESO AÑADE UN SEGUNDO REMOTE. Muestra un pantallazo tanto del repositorio en BitBucket como de git remote en el repositorio local. Añade aquí la url donde pueda verlo.

- Subir el repositorio de la última práctica Git a BitBucket.
- Añadir un **segundo remoto** usando el comando:

```bash
git remote add bitbucket https://usuario@bitbucket.org/usuario/repositorio.git

---

5-En el servidor GitHub:

i-Realiza una búsqueda de todos tus repositorios 
(user:USERNAME)

user:USERNAME

ii-Busca un repositorio tuyo con muchos commits y muestra un par de pantallazos del apartado Insights, incluyendo el apartado Network.

## De interés
Fundamentos-de-Git-Trabajar-con-Remotos
BitBucket
searching-for-repositories
viewing-a-repositorys-network