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

