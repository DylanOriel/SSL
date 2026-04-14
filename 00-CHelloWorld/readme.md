# TP 00-CHelloWorld:
---

## COMPILACION
|  |  |
| :--- | :--- |
| **Compilador** | GCC |
| **Versión del Compilador** | 14.2.0 |
| **Estándar de C** | C17 |

---
## Generar ejecutable y Makefile
Para generar el .exe y mostrar el resultado en la terminal se uso el siguiente comando
```
gcc -o hello hello.c
./hello.exe
```
Para mostrar el resultado en un archivo de texto se hizo
```
./hello.exe < hello.c > hola.txt
```
Por ultimo se creo un archivo tipo Makefile con los mismo comandos para generar el .exe y dos regla adicionales, una que ejecuta el archivo y otra lo borra
```
hello: hello.o
	gcc hello.o -o hello -std=c23

hello.o: hello.c
	gcc -c hello.c -o hello.o

run: hello
	./hello

clean:
	rm -f hello hello.o
```
