
all: mmaplib migration

CXX=g++
CC=gcc

mmaplib: mmaplib.c
	$(CC) -fpic -c mmaplib.c
	$(CC) -fpic -shared -o libmmap.so mmaplib.o

migration: migration.c
	$(CC) -fpic -c migration.c #-D_STOPMIGRATION
	$(CC) -fpic -shared -o libmigration.so migration.o

install:
	sudo cp *.so /usr/local/lib
	sudo cp *.so /usr/lib
	sudo cp *.h /usr/local/include
	sudo cp *.h /usr/include
	sudo cp *.h /usr/lib/

clean:
	rm -rf *.o
	rm -rf *.so

