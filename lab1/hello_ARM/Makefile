all: hello

CC=arm-linux-gnueabihf-as 
LD=arm-linux-gnueabihf-ld

hello.o: hello.s
	${CC} hello.s -o hello.o

hello: hello.o
	$(LD) -static hello.o -o hello

run: hello
	qemu-arm -L /usr/arm-linux-gnueabihf ./hello

clean:
	rm hello hello.o
