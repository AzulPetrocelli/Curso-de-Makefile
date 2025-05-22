#Definimos variables y las aplicamos en el Makefile anterior
OBJS = main.o salida.o calculadora.o
BINARY = programa

#Variable que contiene un flag de C
CFLAGS = -g -Wall

#Esta regla ejecuta dos reglas
all: $(BINARY) clean

#Esta regla compila el programa principal
programa: $(OBJS)
		gcc -o $(BINARY) $(OBJS)

#Elimina todos los archivos .o
clean: 
		rm -f $(BINARY) *.o


#Contenido nuevo---------------------------------------------------------

#Creamos los archivos .o de los que depende la regla programa

#main.o: main.c funciones.h
#salida.o: salida.c funciones.h
#calculadora.o: calculadora.c funciones.h

#En lugar de lo de arriba usamos un patron

#De todos los .o buscame su PRIMERA($<) dependencia .c
%.o: %.c
		gcc $(CFLAGS) -c $<

#De todos los .o buscame su TODAS($?) sus dependencias .c
%.o: %.c
		gcc $(CFLAGS) -c $?

#Si tenemos los .c en una carpeta1 y
# queremos que los .o se guarden en una carpeta2

#carpeta1/%.o: carpeta2/%.c

#Lo mismo podemos hacer con programa
#Esta regla compila el programa principal
programa: $(OBJS)
		gcc -o $(BINARY) $?

# NOTA: el @ representa el nombre de la regla
programa: $(OBJS)
		gcc -o $@ $?