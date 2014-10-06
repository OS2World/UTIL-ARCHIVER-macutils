CFLAGS =	-O $(CF)
CRCC =	arc.c ccitt.c kermit.c binhex.c ccitt32.c zip.c
CRCO =	arc.o ccitt.o kermit.o binhex.o ccitt32.o zip.o

libcrc.a:	$(CRCO)
	ar r libcrc.a $(CRCO)
	ar s libcrc.a 

clean:
	-rm -f $(CRCC) $(CRCO) libcrc.a makecrc makecrc.o

$(CRCC):	makecrc.exe
	./makecrc

makecrc.exe:	makecrc.o
	$(CC) -O -o makecrc.exe makecrc.o

arc.o:	arc.c
ccitt.o:	ccitt.c
kermit.o:	kermit.c
binhex.o:	binhex.c
ccitt32.o:	ccitt32.c
zip.o:		zip.c

