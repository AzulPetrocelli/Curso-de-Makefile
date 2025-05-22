#Esta regla ejecuta dos reglas
all: programa clean

#Esta regla compila el programa principal
programa: main.o salida.o calculadora.o
		gcc -o programa main.o salida.o calculadora.o

#Creamos los archivos .o de los que depende la regla programa
main.o: main.c funciones.h
		gcc -c main.c

salida.o: salida.c funciones.h
		gcc -c salida.c

calculadora.o: calculadora.c funciones.h
		gcc -c calculadora.c

#Elimina todos los archivos .o --> No tiene dependencias por lo que
#se la denomina una REGLA FICTICIAS
clean: 
		rm -f programa *.o