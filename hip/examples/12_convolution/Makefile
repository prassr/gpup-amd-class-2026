# ------------------------------

HIPCC    = hipcc
OFFLOAD_ARCH ?= gfx1100,gfx1150,gfx1151,gfx1201
HIPFLAGS      = --offload-arch=$(OFFLOAD_ARCH)

# ------------------------------

convolution: convolution.o
	$(HIPCC) $(HIPFLAGS) convolution.o -o convolution

convolution.o: convolution.cpp
	$(HIPCC) $(HIPFLAGS) -c convolution.cpp

.PHONY: clean

clean:
	rm -f convolution *.o
