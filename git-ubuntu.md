##Instalar Git en Linux 
```
sudo apt-get install git
```

##Configurar Nombre y Correo electrónico 

```
git config --global user.name "José Alberto"
git config --globa user.email "<jasilva15@gmail.com>"
```

Crear repositorio local en el ordenador. Para esto se necesita tener ya definida un directorio donde se van a guardar estos repositorios. Dentro de directorio:

```
git init.
```

Se creará una carpeta .git que es donde se guardaran todos los archivos del repositorio. En la mayoría de las veces esta carpeta está oculta.

Si se quiere clonar repositorios
Si se quiere clonar repositorios

git clone ~/Dropbox/repositorio.git
git clone http://github.com/torvalds/linux

El lugar donde se guardan los archivos se llama directorio de trabajo, aquí podemos crear todos los archivos que se trabajan y modifican, sin embargo, para poder Añadir estos archivos a git hay que añadirlos a el Staging Index. El Staging Index es un área temporal donde añadimos archivos cuyos cambios estamos a punto de enviar a git en forma de commit. Aquí el funcionamiento de git.

-Modificar archivos dentro del directorio de trabajo.
-Seleccionar aquellos archivos cuyos cambios queremos enviar y agregarlos al Staging Index.
-Confirmar ("commit") esos cambios para que se almacenen en el repositorio.

Para añadir archivos escribimos
```
git add main.c
```

Para añadir todos los archivos del area de trabajo usamos:
git add .

Para ver el estado del staging index teleamos lo siguiente:
git status

Ahora enviaremos los cambios al repositorio con el commit

git commit
Con esto se abrirá un archivo de texto tode podemos añadir comentarios breves sobre los cambios que se estan aplicando. Debe abarcar ciertos parámetros:
