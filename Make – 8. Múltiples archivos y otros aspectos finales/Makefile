#Incluir multiples makefiles

#include carpeta1/makefile1 carpeta2/makefile2

#Definimos variables y las aplicamos en el Makefile anterior
# Con \ ignoramos el salto de barra, util si tenemos muchos archivos
BINARY = programa
OBJS = main.o \
	   salida.o\
	   calculadora.o

#Variable que contiene un flag de C
CFLAGS = -g -Wall

#Esta regla ejecuta dos reglas
all: programa clean

#Esta regla compila el programa principal
programa: $(OBJS)
		gcc -o $@ $?

#De todos los .o buscame su TODAS($?) sus dependencias .c
%.o: %.c
		gcc $(CFLAGS) -c $< -o $@

#Elimina a programa y a todos los archivos .o
clean: 
		rm -f $(BINARY) *.o