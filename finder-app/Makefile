# Makefile for writer.c
# Author: Guruprashanth Krishnakumar, gukr5411@colorado.edu
# Date: 09/04/2022
INCLUDE_DIRS = 
LIB_DIRS = 
# CROSS_COMPILE variable initially set to nothing. Will be over-written if value is passed in the command-line.
CROSS_COMPILE=
cc=gcc

CDEFS=
# Compile at O0 by default
CFLAGS= -O0 -g $(INCLUDE_DIRS) $(CDEFS)
LIBS= 

HFILES= 
CFILES= writer.c

SRCS= ${HFILES} ${CFILES}
OBJS= ${CFILES:.c=.o}

all:	writer

# Remove all .o files and the writer executable
clean:
	-rm -f *.o *.d
	-rm -f writer

# native build if no args are passed, build for the specified target in case args are passed.
writer: writer.o
	$(CROSS_COMPILE)$(cc) $(LDFLAGS) $(CFLAGS) -o $@ $@.o

depend:

.c.o:
	$(CROSS_COMPILE)$(cc) $(CFLAGS) -c $<
