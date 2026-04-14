hello: hello.o
	gcc hello.o -o hello -std=c23

hello.o: hello.c
	gcc -c hello.c -o hello.o

run: hello
	./hello
	
clean:
	rm -f hello hello.o