##Instalar Git en Linux 
```
sudo apt-get install git
```

##Configurar Nombre y Correo electrónico 
```
git config --global user.name "José Alberto"
git config --global user.email "<jasilva15@gmail.com>"
```

Crear repositorio local en el ordenador. Para esto se necesita tener ya definida un directorio donde se van a guardar estos repositorios. Dentro de directorio:
```
git init.
```

Se creará una carpeta .git que es donde se guardaran todos los archivos del repositorio. En la mayoría de las veces esta carpeta está oculta.

Si se quiere clonar repositorios
```
git clone ~/Dropbox/repositorio.git
git clone http://github.com/torvalds/linux
```

El lugar donde se guardan los archivos se llama directorio de trabajo, aquí podemos crear todos los archivos que se trabajan y modifican, sin embargo, para poder Añadir estos archivos a git hay que añadirlos a el **Staging Index**. El Staging Index es un área temporal donde añadimos archivos cuyos cambios estamos a punto de enviar a git en forma de commit. Aquí el funcionamiento de git.

1. Modificar archivos dentro del directorio de trabajo.
1. Seleccionar aquellos archivos cuyos cambios queremos enviar y agregarlos al Staging Index.
1. Confirmar ("commit") esos cambios para que se almacenen en el repositorio.

Para añadir archivos escribimos
```
git add main.c
```

Para añadir todos los archivos del area de trabajo usamos:
```
git add .
```

Para ver el estado del staging index teleamos lo siguiente:
```
git status
```

Ahora enviaremos los cambios al repositorio con el commit
```
git commit
```

Con esto se abrirá un archivo de texto tode podemos añadir comentarios breves sobre los cambios que se estan aplicando. Debe abarcar ciertos parámetros:

1. Por que se ha hecho este cambio?
1. Que cambios se han hecho? Describir un poco esos cambios concretos
1. Que consecuencias de espera que tenga ese cambio?

Hay que considerar lo siguiente:
* La primera línea del mensaje es un resumen del commit, no debe tener mas de 50 caracteres. Se puede escribir en imperativo (ej: "añade X", "corrige Y").
* La segunda línea en blanco.
* A partir de la tercera línea va el cuerpo del mensaje, es recomendable no dejar que cada línea tenga más de 72 caracteres, por lo que será necesario poner saltos de línea a mano.

Ejemplo de momentario:
```
1     Añade funciones de cálculo
2
3     Este cambio agrega funciones para hacer cálculos con los numeros que
4     el usuario proporcione. Con estas funciones se espera poder manipular
5     todos los datos que se necesitan para crear los informes mensuales.
6
7     Se cea un conjunto de funciones para realizar las cuetro operaciones
8     elementales: suma, resta, multiplicación y división. Las tres primeras
9     aceptan dos números enteros y devuelven un npumero entero. la función
10    división acepta dos números enteros y un puntero a un número entero
11    donde se guardara el resultado y devuelve un número distinto de cero
12    si se ha dividido bien, y cero si se ha intentado dividir entre cero.
```

