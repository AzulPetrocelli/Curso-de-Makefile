#Definimos variables y las aplicamos en el Makefile anterior
OBJS = main.o salida.o calculadora.o
BINARY = programa

#Esta regla ejecuta dos reglas
all: $(BINARY) clean

#Esta regla compila el programa principal
programa: $(OBJS)
		gcc -o $(BINARY) $(OBJS)

#Creamos los archivos .o de los que depende la regla programa
# Makefile sabe como compilar archivos .o y otros por lo que no
# hace falta que le demos intrucciones para compilarlo solo
# lo que necesita para hacerlo

main.o: main.c funciones.h

salida.o: salida.c funciones.h

calculadora.o: calculadora.c funciones.h

#Elimina todos los archivos .o
clean: 
		rm -f $(BINARY) *.o