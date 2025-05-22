#Definimos variables y las aplicamos en el Makefile anterior
OBJS = main.o salida.o calculadora.o
BINARY = programa

#Variable que contiene un flag de C
CFLAGS = -g -Wall

#Podemos meter variables en otras:

#Variable de expancion recursiva 
#(toma el valor redefinido de x)
x = Hola
y = $(x) Adios
x = Adios

#Variable de expancion simple
#(no toma el valor redefinido de x)
x = Hola
z := $(x) Adios
x = Adios

#Nota: el @ al principio del echo es para que no 
# me muestre la regla que esta ejecutando en pantalla 
imprimir:
		@echo Variable de expancion recursiva x: $(x)
		@echo Variable de expancion recursiva y: $(y)
		@echo Variable de expancion simple z: $(z)

#Esta regla ejecuta dos reglas
all: $(BINARY) clean

#Esta regla compila el programa principal
programa: $(OBJS)
		gcc -o $(BINARY) $(OBJS)

#Creamos los archivos .o de los que depende la regla programa
main.o: main.c funciones.h
		gcc $(CFLAGS) -c main.c

salida.o: salida.c funciones.h
		gcc $(CFLAGS) -c salida.c

calculadora.o: calculadora.c funciones.h
		gcc $(CFLAGS) -c calculadora.c

#Elimina todos los archivos .o --> No tiene dependencias por lo que
#se la denomina una REGLA FICTICIAS
clean: 
		rm -f $(BINARY) *.o