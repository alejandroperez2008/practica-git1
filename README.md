# practica-git1
## 1 ¿Qué es Git?
![Descripción de la imagen](/IMAGES/GIT.PNG)
Git es un sistema de control de versiones distribuido. Sirve para registrar los cambios que se realizan en los archivos de un proyecto a lo largo del tiempo.

Control de versiones: Permite "viajar en el tiempo" para recuperar versiones anteriores, ver quién cambió qué línea de código y mantener un historial organizado.

Distribuido: Significa que cada desarrollador tiene una copia completa del repositorio (con todo el historial) en su propio ordenador, por lo que no depende de estar conectado a un servidor central para trabajar, hacer confirmaciones o revisar el historial.

## 2 ¿Cuál es el flujo de trabajo de Git?
![Descripción de la imagen](/IMAGES/FLUJO.PNG)
El flujo de trabajo básico se divide en cuatro áreas principales por las que viaja el código desde que se escribe hasta que se guarda en la nube:

Working Directory (Directorio de trabajo): Es la carpeta local en tu ordenador donde creas y modificas tus archivos. Los cambios aquí están "sucios" o sin rastrear hasta que decides prepararlos.

Staging Area (Área de preparación): Una zona temporal donde seleccionas e indexas qué cambios específicos quieres incluir en tu próximo guardado.

Local Repository (Repositorio Local): La base de datos oculta en tu máquina (.git) donde los cambios se guardan de forma permanente e histórica en forma de "commits".

Remote Repository (Repositorio Remoto): El servidor en la nube (como GitHub o GitLab) donde subes tus commits locales para compartirlos con el equipo o tener una copia de seguridad.

## 3 Comandos realizados durante la práctica
![Descripción de la imagen](/IMAGES/COMANDOS.PNG)
A continuación se detalla qué hace cada comando técnico de Git (y cómo se reflejan en la interfaz visual de SourceTree):

git add: Toma los cambios del Working Directory y los mueve al Staging Area.

En SourceTree: Equivale a pulsar el botón Stage All o seleccionar un archivo y subirlo a la sección de arriba (Staged files).

git commit: Guarda de forma permanente los archivos que estaban en el Staging Area dentro del Repositorio Local, asignándoles un identificador único y un mensaje descriptivo.

En SourceTree: Equivale a escribir en el cuadro de texto inferior y pulsar el botón Commit abajo a la derecha.

git push: Sube los commits que has acumulado en tu Repositorio Local hacia el Repositorio Remoto en la nube.

En SourceTree: Es el botón Push de la barra superior.

git fetch: Consulta el Repositorio Remoto para comprobar si otros compañeros han subido cambios nuevos, descargando esa información sin modificar ni tocar tu código local.

En SourceTree: Es el botón Fetch. Te avisa si hay novedades mostrando números en el botón de Pull.

git pull: Descarga los cambios nuevos del Repositorio Remoto y los fusiona de inmediato en tus archivos locales. Es una combinación directa de ejecutar un git fetch seguido de un git merge.

En SourceTree: Es el botón Pull.

git merge: Junta dos líneas de tiempo o ramas de desarrollo distintas para unificarlas en una sola.

En SourceTree: Es el botón Merge. Lo usamos en la práctica para unir a la fuerza la rama descargada de GitHub con tu rama del PC.

## 4 ¿Qué es un conflicto de Git, qué lo causa y cómo solucionarlo?
![Descripción de la imagen](/IMAGES/SOURCE.PNG)
¿Qué es y qué lo causa?
Un conflicto ocurre cuando Git no puede fusionar dos versiones de código de manera automática y se detiene para no destruir el trabajo de nadie.

Se causa principalmente cuando dos entornos cambian la misma línea del mismo archivo con textos diferentes y luego intentan unirse.