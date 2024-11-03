##   Tarea 1
## Introduccion a GitHub
### Descripcion 
El objetivo es crear un repositorio local y remoto para darle seguimiento a un codigo programado en 
*Java* el cual su unica funcion es imprimir el mensaje de **Hola Mundo**; Ya que es una introduccion 
se pondran en practica los comandos basicos de git y nuestro repositorio lo guardaremos en un proveedor 
de alojamiento de git llamado **GitHub** 

## Instrucciones de uso del programa "HolaMundo.Java"
Para esta introdiccion estamos utilizando el editor de codigo Visual Studio Code, este editor tiene una
herramienta muy practica para ejecutar programas con un simple boton situado en la parte superior derecha

![alt text](https://github.com/Vazquez-Goto/Tarea1v2/blob/d74d449c11cb7ee047fddf8428a23829cd299771/Imagenes/Imagen1.png )

Al ejecutarlo podemos observar en la terminal de que en efecto el programa hace lo que deberia

![alt text](https://github.com/Vazquez-Goto/Tarea1v2/blob/d74d449c11cb7ee047fddf8428a23829cd299771/Imagenes/Imagen2.png)

Tambien existe otra manera de ejecutar el programa desde la terminal del editor, para abrirla podemos usar
el comando **CTRL + Ñ**, si estas en windows, **CTRL + SHIFT + Ñ** si es que quieres una nueva terminal o
de manera manual en la parte superior se encuentra una pestaña llamada *View* despues seleccionamos la opción 
*Terminal* y esta se abrira automáticamente 

![alt text](https://github.com/Vazquez-Goto/Tarea1v2/blob/d74d449c11cb7ee047fddf8428a23829cd299771/Imagenes/Imagen3.png)

Ahora escribiremos en la terminal el comando *cd* y escribiremos entre comillas simples la direccion de la carpeta 
donde se encuentra el archivo *.java* como se muestra a continuacion:

![alt text](https://github.com/Vazquez-Goto/Tarea1v2/blob/d74d449c11cb7ee047fddf8428a23829cd299771/Imagenes/Imagen4.png)

Siguiendo de esto utilizaremos el siguiente comando para crear el ejecutable *javac NOMBRE_ARCHIVO.java* 
y para ejecutarlo es *java NOMBRE_ARCHIVO* se observara de la siguiente manera:

![alt text](https://github.com/Vazquez-Goto/Tarea1v2/blob/d74d449c11cb7ee047fddf8428a23829cd299771/Imagenes/Imagen5.png)

o bien presionar F5

## COMANDOS DE GIT UTILIZADOS
Estos comandos los utilizamos en la terminal **Git Bash** que previamente instalamos ya sabiendo esto podemos
comenzar 
### Inicializacion del Cliente de git
+ *git config --global user.name "Nombre Usuario"* 
+ *git config --global user.email "Correo @ email.com"* este correo es con el que previamente se registro en la pagina
                                                      de Git Hub.
### Crear un repositorio local
Primero crearemos una carpeta en la cual guardaremos nuestro repositorio, despues en la terminal Git Bash utilizaremos
el comando *cd* y entre comillas dobles pondremos la direccion de la carpeta donde guardaremos el repositrio ejemplo
***cd "DIRECCION_CARPETA"*** ya que la terminal se encuentra en la carpeta podemos empezar.
Tambien previamente tendremos que haber creado un repositorio en la pagina de github ya que necesitaremos utilizar
el URL que este nos proporciona para enlazarlo donde se alojara este.

+ *git init* este comando creara una carpeta .git
+ *git remote add ALIAS URL-ALMACENAMIENTO-REMOTO* Enlaza la carpeta con el almacenamiento de github normalmente ALIAS = origin

### Enviar cambios al repositorio remoto
+ *git add -A* Este comando sirve para poner en espera a todos los elementos del repositorio local antes de enviarlos al repositorio remoto
+ *git add NOMBRE_ARCHIVO.extencion* Sirve para subir un archivo en especifico al repositorio remoto
+ *git status* Sirve para observar el proceso que van tomando los archivos al momento de querer hacer cambios al repositorio remoto
+ *git commit -m "MENSAJE DEL COMMIT"* Su funcion es confirmar que se esta queriendo mandar algo al repositorio local
+ *git push ALIAS NOMBRE-RAMA* Despues de confirmar con "git commit" ya podemos subir los cambios al repositorio remoto con este comando.
  ALIAS = origin, como previamente mencionamos utilizamos ese alias, NOMBRE-RAMA = master.
### Recibir datos de un repositorio remoto
Para ello crearemos una carpeta llamada "Proyecto-Casa" y abriremos otra terminal Git Bash y la dirijiremos con el comando *cd* a la
direcccion donde se encuentra esta ya teniendo eso podemos crear nuestro clon del repositorio.
+ *git clone URL-REPOSITORIO-GITHUB* Sirve para descargar un clon del repositorio remoto en el computador
+ *git pull ALIAS NOMBRE-RAMA* Su funcion es para actualizar el repositorio local descargando asi los archivos nuevos o actualizando los
  ya existentes
   
### Notas .gitignore
+ *touch .gitignore* Sirve para crear un archivo el cual su funcion es hacer que git ignore ciertos archivos al momento de
  hacer cambios al repositorio remoto
Ya creado este archivo con nuestro editor de codigo VS Code podemos editar su contenido y hay ciertos comandos
los cuales nos sirven para que funcione correctamente

![alt text](https://github.com/Vazquez-Goto/Tarea1v2/blob/d74d449c11cb7ee047fddf8428a23829cd299771/Imagenes/Imagen6.png)

  Para fines de aprendizaje cree un archivo con extencion *.log* llamado "debug" el cual vamos a querer que el archivo con extencion *.gitignore*
  evite que se suba al repositorio

  Primero cree el *archivo.gitignore* y escribi dentro de el el comando ***.log** y al momento de querer hacer cambios al repositorio remoto
  observamos que este cumple con su funcion.
  
  ![alt text](https://github.com/Vazquez-Goto/Tarea1v2/blob/d74d449c11cb7ee047fddf8428a23829cd299771/Imagenes/Imagen7.png)
  
  Despues elimine el archivo .gitignore y podemos observar que ya nada detiene que este se suba al repositorio remoto:
  
  ![alt text](https://github.com/Vazquez-Goto/Tarea1v2/blob/d74d449c11cb7ee047fddf8428a23829cd299771/Imagenes/Imagen8.png)
  
  Muy bien para verificar que no esta en el repositorio remoto desde la pagina de GitHub podemos observar que no se encuentra ningun "debug.log"
  
  ![alt text](https://github.com/Vazquez-Goto/Tarea1v2/blob/d74d449c11cb7ee047fddf8428a23829cd299771/Imagenes/Imagen9.png)
  
