# Bases-de-datos-NoSQL

Bienvenido al curso! 

Introducción a los datos semi-estructurados y no estructurados. 

A continuación te dejo un serie de instrucciones para que puedas subir tus tareas al repositotio de la clase. 

## Paso 0: Configuración de tu cuenta de GitHub de manera local 

Si nunca haz configurado tu cuenta de GitHub de manera local, sigue las siguientes instrucciones, de lo contario ve al paso 1.

Debes tener una cuenta creada con un correo para el sitio oficial de Github.

Antes que nada considera el sistema operativo con el cuenta tu ordenador. 

- Para usuarios con **Windows** 

Para utilizar Git de manera eficiente es necesario descargar alguna de las siguientes aplicaciones:

- Git Bash
[Descargar Git Bash](https://git-scm.com/downloads)
- Git desktop
[Descargar Github Desktop](https://desktop.github.com/)

Para cuestiones del curso vamos a trabajar con Git Bash. 

En este caso sigue las instrucciones que se encuentran en el link, para descargar de manera correcta la aplicación. 

- Abre la aplicación de Git Bash, se abriria una terminal donde ahora podras ejecutar comandos de Linux. 

- Configura tu cuenta de Git con los siguientes comandos 

    - git config --global user.name "Tu nombre o usuario" 
    - git config --global user.email "tu-email@ejemplo.com"

**Opcional** Puedes configurar una clave ssh ya que es más seguro que el protocolo HTTP. **Warning:** Solo en caso de que tengas un computadora propia. 

- Para usuarios Mac 

1. Descarga el instalador:

Visita la página oficial de Git: https://git-scm.com/download/mac

Descarga el instalador más reciente para macOS.

Instala Git:

Abre el archivo descargado (.dmg) y sigue las instrucciones del instalador.

Por lo general, puedes dejar las opciones predeterminadas.

Verifica la instalación:

Abre la aplicación Terminal (la puedes encontrar en Aplicaciones > Utilidades).

Escribe el siguiente comando y presiona Enter: git --version
Si Git se instaló correctamente, verás la versión de Git instalada.

2. Usando Homebrew:

Instala Homebrew (si no lo tienes):

Homebrew es un administrador de paquetes para macOS que facilita la instalación de software.

Abre la Terminal y pega el siguiente comando: /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

Sigue las instrucciones que se te muestren en la terminal.

Instala Git con Homebrew:

Una vez que Homebrew esté instalado, ejecuta el siguiente comando en la Terminal: brew install git

Verifica la instalación:

Al igual que antes, usa el comando git --version para confirmar que la instalación fue exitosa.


## Paso 1: Fork del repositorio del curso

Lo primero que tienes que hacer es ingresar con una cuenta desde e sitio ofiical de [GitHub](https://github.com/), una vez que inicies sesión con tu cuenta, busca el link del repositotio de la clase [Repositorio de la clase](https://github.com/RJDom10/Bases-de-datos-NoSQL) . 

Ahora que te encuentras en el repositorio de la clase en la parte superior derecha da click en el boton que dice **Fork**, puedes dejar el nombre tal cual como esta o lo puedes modificar a tu gusto, posterior a esto en la parte inferior da cilck en **Create Fork**. 

Se abrirá una copia exacta del repositorio del curso, esto lo puedes confirmar pues en la parte superior verás tu usuario junto con el nombre que usaste cuando creaste el Fork, se verá así: Juan10/Bases-de-datos-NoSQL.

En tu repositorio, es decir la copia, da cilck en **Sync fork** para sincronizar con el repositorio original es decir este. 

## Paso 2: Terminal 

Ahora en la terminal clona el repositorio que acabas de crear en tu cuenta de GitHub, entra en la sitio de GitHub, abre tu repositorio que acabas de copiar en tu perfil, da click en el boton code y copia la dirección HTTPS o SSH (en caso de que hayas configurado una llave ssh en tu computadora local) y ejecuta el siguiente comando 

- git clone https://github.com/"Tu usuario de git"/Bases-de-datos-NoSQL.git

Como ejemplo: https://github.com/JuanPerez/test_repository_github.git

De esta manera tendras ahora un copia de todos los archivos que existen en el repositorio de la clase en tu computadora local. 

Ahora muevete al directorio de la clase con el siguiente comando

- cd "Nombre del repositotio"

Como ejemplo: cd Bases-de-datos-NoSQL/ 

Ahora en este momento tienes un repositorio origin el cual apunta a tu repositotio personal. 

Necesitamos agregar ahora un repositorios upstream el cual es el original. 

**¿Qué significa origin y upstrream?**

+ origin: Es el remoto por defecto asociado a tu fork personal (clonado desde tu cuenta de GitHub.)

+ upstream: Suele referirse al repositotio original del que hiciste fork (para sincronizar cambios). 

Utiliza el siguiente comando para agregar el repositorio original 

git remote add upstream https://github.com/RJDom10/Bases-de-datos-NoSQL.git

una vez hecho esto ahora ejecuta el siguiente comando para ver el repositorio original y el upstream: 

- git remote -v 

Tendrás que ver el origin y el upstream. 

En origin tendras la ruta con tu repoisitotio personal. Mientras que en el upstream verás la ruta del repositorio original. 

## Paso 3: Creación de tu propia rama 

Ahora en la misma terminal vamos a crear las ramas, en la cual será donde trabajemos y subirás los archivos o directorios de tus tareas. 

Cambia y crea la rama de tu grupo segun corresponda: Grupo-402, Grupo-403. 

Utliza el siguiente comando: 

git branch Grupo-40* 

Puedes ejecutar: 

- git branch

Para listar todas las ramas que tienes, la rama actual en la que te encunetras estará resaltada con un * o con otro color. Cambia a la rama de tu grupo con: 

- git checkout Grupo-40*

y ahora crea la rama con tu nombre y apellido como por ejemplo: 

- git branch -b JorgeDominguez-40*

Esto te permite crear y además cambiarte a la rama que acabas de crear. 

En este punto en el explorador de archivos debes tener una carpeta con el nombre del repositorio en la ruta donde empezaste a crear la copia del repositorio. 

En esta carpeta agrega los archivos, que vas a subir, ya sea imágenes, archivos, etc. 

**Warning: Siempre que subas los archivos asegurate de estar en tu rama con tu nombre**

## Paso 4: Sube tus tareas 

Ahora que te encuentras en tu rama personal con tu nombre, sube los archivos que necesitas para entregar la tarea. 

Una vez que los hayas guaradado, puedes revisar el estatus de tus archivos con el siguiente comando:

- git status

Una vez que aparecen archivos en color rojo (por lo general aparecen en este colar y además menciona Archivos sin seguimineto: Usa "git add 'tu-archivo'... "), deberás agregarlos usando las siguientes instrucciones:

- git add nombre-del-archivo-o-carpeta # para agregar un solo archivo o 

- git add . # para agregar todos los archivos que tienes sin seguimiento. 

Hacer un commit con un mensaje descriptivo: 

- git commit -m "Aquí tu mensaje"

Subir cambios a GitHub (para la primera vez), en futuras ocasiones basta con git push. 

- git push --set-upstream origin JorgeDominguez-40* <---- esta la rama que hiciste con tu nombre y grupo. 

## Paso 5: Pull Request 

Ahora que ya haz realizado el push y el commit de tus archivos, ve a al sitio de GitHub. y en tu repositorio fijate que aparece un boton de color verde con Compare and Pull Request o en la parte intermedia aparece un botón con "Contribute" da click en cualquiera de los dos deja un mensjae breve de lo que haz hecho.

 **Importante: fijate que en esta pantalla debe aparecer en la parte de arriba que vas a hacer el PR desde la rama con tu nombre (lado izquierdo) hacia la rama de tu grupo correspondiente (lado derecho), da click en main ya que es la rama por defecto y selecciona la rama que corresponde a tu grupo.**
 
Los cambios que hiciste, o de los archivos que subiste, etc, y por último da en Click en Create Pull request.

Por el momento es todo espera la respuesta de tu profesor. 




