#
# Makefile for math and optical engineering functions and subroutines
#
# Ulf GRIESMANN, April 2020
#

fSRC = bicubic.f  math.f  opteng.f  sort.f  svd.f  tilter.f

FOBJ = $(fSRC:.f=.o)

# targets
all: libkmath

libkmath: $(FOBJ)
	ar r libkmath.a $?
	ranlib libkmath.a
	mv libkmath.a ../lib

%.o: %.f
	$(FC) -c $(FFLAGS) $(IFLAGS) $<

clean:
	rm -f *.o *~
