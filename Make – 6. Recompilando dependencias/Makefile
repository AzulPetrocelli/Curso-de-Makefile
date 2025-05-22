#Definimos variables y las aplicamos en el Makefile anterior
OBJS = main.o salida.o calculadora.o
BINARY = programa

#Esta regla ejecuta dos reglas
all: $(BINARY) clean

#Esta regla compila el programa principal
programa: $(OBJS)
		gcc -o $(BINARY) $(OBJS)

#Creamos los archivos .o de los que depende la regla programa
main.o: main.c funciones.h

salida.o: salida.c funciones.h

calculadora.o: calculadora.c funciones.h

#Elimina todos los archivos .o
clean: 
		rm -f $(BINARY) *.o


#IMPORTANTE: Makefile recompila dependencias SOLAMENTE cuando
# el archivo objeto es mas viejo que el archivo fuente, es
# decir, cuando el archivo fuente es modificado

#Para ver la fecha de modificacion de los archivos lo hacemos
# con el comando
# ls -l

#Podes probarlo modificando cualquiera de los archivos .c