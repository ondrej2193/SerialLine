IDIR =../include
CC=g++
CFLAGS=-I$(IDIR)

ODIR=obj
LDIR =../lib


_DEPS = serial.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))

_OBJ = SendSerial.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))


$(ODIR)/%.o: %.cpp $(DEPS)
	$(CC) -std=c++11 -Wall -c -g -ggdb -O0 -o $@ $< $(CFLAGS)

SendSerial: $(OBJ)
	$(CC) -o $@ $^ $(CFLAGS) $(LIBS)

.PHONY: clean

clean:
	rm -f $(ODIR)/*.o *~ core $(INCDIR)/*~ 
