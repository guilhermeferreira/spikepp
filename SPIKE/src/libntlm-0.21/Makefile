CFLAGS=-Wall -g

DEST=/usr/local
LIBDEST=$(DEST)/lib
INCDEST=$(DEST)/include

SRCS=smbdes.c smbencrypt.c smbmd4.c smbutil.c
OBJS=smbdes.o smbencrypt.o smbmd4.o smbutil.o

libntlm.a: $(OBJS)
	ar cru libntlm.a $(OBJS)
	ranlib libntlm.a

install: libntlm.a ntlm.h
	install libntlm.a $(LIBDEST)
	install ntlm.h $(INCDEST)

clean: 
	rm -f *.a *.o *~ *.bak \#*\#

depend:
	makedepend $(SRCS)
# DO NOT DELETE


