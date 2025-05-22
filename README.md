# Curso de Makefile

## Make 2
*  `Reglas:` comando que sigue una serie de intrucciones podes llamarla desde la consola usando Make "Nombre de la Regla".
*  `Dependencias:` archivos de los que va a depender para realizar su tarea,por ejemplo archivos.o u otra regla.
*  `Instrucciones:` instrucciones de codigo que va a seguir para cumplir la tarea para la que fue creada, ej compilar un archivo con gcc.

## Make 3
*   Incluir dos o mas reglas en una.
*   Crear archivos .o para los .c (uno por uno)
*   Borrar archivos .o (los seleccionamos con *.o) y programa


## Make 4
*   Definicion de variables, podemos guardar flags y nombres de archivos.
*   Si ponemos @ al principio de una palabra no la muestra por pantalla.
*   Tipos de Variables:
    *   `Variable de expancion recursiva:` si esta compuesta por otra variable podemos modificarla en cualquier momento.
    *   `Variable de expancion simple:` si esta compuesta por otra variable NO podemos modificar esa variable.

## Make 5
*   Reducimos el codigo, los makefile saben compilar archivos .o, no necesita que le pasemos las intrucciones de como hacerlo, solo las dependencias necesarias.

## Make 6
*   Makefile recompila dependencias SOLAMENTE cuando el archivo objeto es mas viejo que el archivo fuente, es decir, cuando el archivo fuente es modificado.
*   ara ver la fecha de modificacion de los archivos lo hacemos con el siguiente comando: `ls -l`

## Make 7
*   Denotamos las reglas y las dependencias e intrucciones usando PATRONES:
    *   $< : Busca la primer dependencia de la regla(va en intrucciones).
    *   $? : Busca todas las dependencias de la regla(va en intrucciones).
    *   $@ : Busca el nombre de la regla(va en intrucciones).
    *   %.extencion: todos los archivos de una extencion que se generan con o dependen de otros.
    *   Tomar un objetivo de una carpeta.
    *   Tomar una dependencia de una carpeta. 

## Make 8
*   Incluir multiples makefiles.
*   Con \ ignoramos el salto de barra.