CC=gcc

PROGS=p1 p2 p3 p4

# Linux defaults:
CFLAGS=-ggdb -pedantic -Wall
#CFLAGS=-O4 -Wall
LDFLAGS=-lm

all:	$(PROGS)

p1:	p1.o
p2:	p2.o
p3:	p3.o
p4:	p4.o
	$(CC) $(LDFLAGS) -o $@ $<

%.o:	%.c
	$(CC) $(CFLAGS) -c -o $@ $<

clean:	objclean
	for b in $(PROGS); do if [ -f "$$b" ]; then rm "$$b"; fi done

objclean:
	for obj in p?.o; do if [ -f "$$obj" ]; then rm "$$obj"; fi done
