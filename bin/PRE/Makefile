# Generated automatically from Makefile.in by configure.
SYSOS	:= $(shell uname)

ALL: default
##### User configurable options #####

ifeq "$(SYSOS)" "AIX"
CC          = xlc
CCC         = xlC
F77         = xlf
endif
ifeq "$(SYSOS)" "IRIX64"
CC          = cc
CCC         = CC
F77         = f77
endif
ifeq "$(SYSOS)" "Linux"
CC          = gcc
CCC         = g++
F77         = gfortran
endif
CLINKER     = $(CC)
CCLINKER    = $(CCC)
FLINKER     = $(F77)
FLAGS       = -O2

EXECS = preprocess
default: $(EXECS)

all: default

preprocess: preprocess.o element2.o boundary.o node.o hilbert.o
	$(CCC) $(FLAGS) -o preprocess preprocess.o element2.o \
	boundary.o node.o hilbert.o

clean:
	rm -f *.o *~ PI* preprocess frict.data

.C.o:
	$(CCC) $(FLAGS) -c $*.C

