# Comandos para Ubicación y Contenido

**pwd** &rarr; Mostrar dónde estoy situado.

    Para saber donde estoy, y por lo tanto, para no perderme dentro del terminal de Linux...

**ls**  &rarr;  Mostar archivos y carpetas.

    Es importante saber, que hay que mirar antes de hacer algo...

### Comandos para Moverse entre carpetas

**cd** &rarr; ChangeDirectory. Moverse entre carpetas

    cd Documents      Estoy dentro de una carpeta

    cd ..             Volver hacia atrás

    cd ~              Voy a mi carpeta personal.

**Importante: Si no etoy bien situado, todo puede fallar...**

### Comandos para archivos

**touch** &rarr; Sirve para crear un archivo vacío.

**nano** &rarr; Editar archivo.

      Ctrl + O --> Guardar Documento

      Ctrl + X --> Salir del Documento

### Comando para Ver Contenido

**cat** &rarr; Muestra lo que hay dentro de un archivo.

        Si uso solo cat, se queda esperando...

        Para salir de este estado,    Ctrl + C

### Detener Comandos (Finalizar "Procesos")

**Ctrl + C** &rarr; Detener un proceso.

        NO COPIA UN COMANDO PEGADO COMO EN WINDOWS...

**Ctrl + Shift (Flecha Izq Arriva) + C** &rarr; Copiar archivos, carpetas, etc.

**Importante: También es considerado como un botón de emergencia...**

### Borrar

***rm*** &rarr; borrar archivos

***rmdir*** &rarr; borrar carpetas vacías

***rm -r*** &rarr; borrar carpetas con TODO dentro.

    Usar sólo si estoy segurx de lo que hago...

#### Ideas Clave (IMPORTANTES)

- Linux distingue mayúsculas
- Un archivo no se ejecuta escribiedo su nombre...
- Siempre hay que saber dónde estoy antes de borrar cualquier cosa...
- Linux NO falla, explica lo que ocurre para que podáis solventarlo.
- Mejor lento y entendiendo las cosas, que rápido y mal

### Copiar y Mover archivos

**cp** &rarr; Copiar archivos (el Original NO se pierde)

*Regla Mental*: ***cp = "Hacer una copia y dejar el original donde está"***

Ejemplos:

    cp prueba.txt copia.txt     --> Crea una copia con otro nombre

    cp prueba.txt ..            --> copia el archivo a la carpeta de arriba.

***Importante:***

- El segundo nombre puede ser cualquiera
- Linux no exige "copia" en el nombre
- Si el destino no existe, Linux crea un arhivo con este nombre.

Si algo se se copia con nombre raro &rarr; No es un error, Linux obedece literalmente nuestras instrucciones.

***mv*** &rarr; Se utiliza para Mover o Renombrar archivos

*Regla Mental:* ***mv = "cambiar de lugar o cambiar nombre"***

Ejemplos:

    mv archivo.txt carpeta/                     --> mueve el archivo

    mv mal\_escrito.txt bien\_escrito.txt       --> Renombrar el archivo

    mv archivo.txt Archivo\_Final.txt           --> cambiar el nombre completo.

**Importante: mv NO COPIA, el archivo desaparece del lugar original.**

### Rutas, Subir y Bajar carpetas

**.. (dos puntos)** &rarr; Representar "la carpeta anterior"

***Regla Clave: NO es un comando, es una ruta.***

Correcto:
  - cd ..
  - cp archivo.txt ..

Incorrecto:

  - .. (Sólo no hace nada...)

Entender Errores Comunes

  - "not a directory" --> Estoy intentando entar con cd a un archivo.
  - "No such file or directory"
  - El nombre está mal escrito
  - Falta una letra
  - Estoy en otra carpeta

***Linux no adivina, ejecuta exactamente lo que escribo...***

Renombrar Archivos (corregir errores) &rarr; Esto se hace con ***mv***

Ejemplo:
 
    mv impotate.txt  importante.txt
    No existe "renombrar" el Linux, sólo mover con otro nombre.

  ***Nombres de Archivos Correctos***
  Usar:
- Letras en minúsculas
- guión bajo \_
- Nombres claros

Evitar:
- espacios
- acentos
- Usar la ñ
- Símbolos o caracteres raros...

*Regla de oro: Si necesito comillas para escribir el nombre, el nombre está mal elegido.*

### Permisos (Lectura, Escritura y Ejecución)

***r = read (leer)***

***w = write (escribir / modificar)***

***x = execute (ejecutar / entrar (en carpetas))***

**En carpetas:**

***x = poder entrar en ellas***

***r = ver lo que hay dentro de ellas***

***ls -l &rarr; Mostrar permisos, dueños y tipo de archivos/carpetas***

Ejemplo:

  **drwxrwxr-x**

  ***- d &rarr; directorio***
  ***- rwx &rarr; usuario***
  ***- rwx &rarr; grupo***
  ***- r-x &rarr; otros***

**El orden siempre es : usuario - grupo - otros**

***chmod*** &rarr; cambiar permisos

Ejemplos:
    
    chmod g-w archivo.txt   --> quitar escritura al grupo
    
    chmod 600 archivo.txt   --> sólo el usuario puede leer y escribir
    
    chmod puede cambiar varios permisos en un solo comando.

### Ideas clave que ya empezamos a dominar

  - Linux es literal --> tal y como lo escribo, se ejecuta.
  - Un error de letra crea otro archivo.
  - cp copia, mv mueve o renombra
  - rm borra archivos
  - rmdir sólo carpetas vacías
  - rm -r borra TODO
  - cat sólo muestra Contenido
  - Ctrl + C finaliza comandos / Procesos
  - Importante: Pensar antes de borrar
  - Entender > Memorizar

##############################################################

# Gestión de Paquetes (APT)

La gestión de paquetes en Linux, es un tema clave no solo para el examen de la certificación, sino también en la gestión 
de sistemas Linux en la vida real.

Si sabemos cómo utilizarlo, y sobre todo, cómo aplicarlo y gestionarlo, seremos unos grandes Administradores/as de Software y 
de Sistemas.


**apt-get update** &rarr; Actualizar la lista de programas disponibles en nuestro sistema.

	Que hace:
 		- Actualiza la lista de programas que Linux puede instalar o actualizar.
 		- NO se instala nada
 		- NO actualiza programas
 		- Sólo revisa que versión de X programas es el que existe

	Por qué es importante: Si no hago esto antes, Linux puede instalar versiones antiguas disponibles. 

	Clave para entender y usar este comando: Siempre va ANTES de instalar cualquier cosa, actualizar.
	"Es como preguntar al sistema: ¿qué hay disponible hoy?"


**apt-get upgrade** &rarr; Actualizar programas ya instalados.

	Qué hace:  Actualiza todos los programas instalados a su versión más reciente.

	Qué NO hace: NO instala programas nuevos , ni borra programas...

	Cuándo usarlo: Después de apt-get update

	"Es como decir: actualiza todo lo que ya tengo"


**apt-get install** &rarr; Instalar un programa.

	Qué hace: Instala el programa que yo le pida.

	Ejemplo mental: Instalar algo que no tengo todavía.

	install = traer algo nuevo al sistema.


**apt-get remove** &rarr; Eliminar un programa (sin borrar configuración)

	Que hace: Borrar el programa pero deja archivos de configuración.
	
	Para qué sirve: Si quiero quitar un programa pero tal vez volver a usarlo después, usaré apt-get remove...

	Remove = desinstalar, pero no limpia del todo...

**apt-get purge** &rarr; Elimina un programa COMPLETAMENTE

	Qué hace: Borrar el programa, y también TODOS sus archivos de configuración.

	Para qué sirve: Cuando quiero borrar algo para siempre.

	Purge = eliminar sin dejar rastro.

**apt-get autoremove** &rarr; Limpiar dependencias o paquetes que ya no se usan.

	Qué hace: Elimina librerías y programas que se instalaron como apoyo y que ahora ya no sirven porque
	se han quedado obsoletos o en desuso.

	Cuándo usarlo: Después de upgrade o remove.

	Resultado:
		- Liberamos espacio del disco duro
		- Obtenemos un sistema más limpio
		- Nada se rompe...

	Es la limpieza final del sistema!!!


**sudo (MUY IMPORTANTE)**
	
	&rarr; Lo vamos a usar o utilizar para ejecutar acciones como administrador (es el rey)

	Por qué es necesario: Instalar, borrar o actualizar programas que afectan a todo el sistema.

	Qué significa: Linux me pide permisos porque estoy haciendo algo importante.

	Nota Mental: "Sin sudo, Linux me protege de errores graves"

Orden Correcto (Este flujo es ORO o Canelita en Rama...)

1- sudo apt-get update

2- sudo apt-get upgrade

3- sudo apt-get autoremove

Memorizarlo de las siguiente manera: Actualizo --> Subo --> Limpio


Errores Comunes

	- ap-get --> mal escrito
	
	- apt.get --> mal escrito

	- Sin sudo --> permiso denegado

"Linux no falla: Explica exactamente qué hicimos mal..."



