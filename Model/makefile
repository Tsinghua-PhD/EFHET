CC = g++
CFLAGS = -lm -pthread -O2 -march=native -Wall -funroll-loops -Wno-unused-result -lgsl -lm -lgslcblas

pl_warp: pl_warp.cpp utils.o EFHET.o
	$(CC) $(CFLAGS) -o pl_warp pl_warp.cpp utils.o EFHET.o

utils.o: utils.cpp
	$(CC) $(CFLAGS) -c utils.cpp

EFHET.o: EFHET.cpp
	$(CC) $(CFLAGS) -c EFHET.cpp

clean :
	rm -rf *.o pl_warp
