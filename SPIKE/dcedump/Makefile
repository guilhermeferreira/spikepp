.SUFFIXES: .a .o .c
CC              =  gcc
CFLAGS          =  -Wall -funsigned-char -c -fPIC -ggdb

BINS = ifids dcedump

ALL = $(BINS)

DCE_OBJS = dcedump.o tcpstuff.o

.c.o:
	${CC} ${CFLAGS} ${INCLUDE} $<

all: $(ALL)

ifids: ifids.o tcpstuff.o
	$(CC) -o ifids ifids.o tcpstuff.o

dcedump: $(DCE_OBJS)
	$(CC) -o dcedump $(DCE_OBJS)


clean:
	rm -f *~ *.bak
	rm -f include/*~ include/*.bak
	rm -f *.o
	rm -f dcedump


