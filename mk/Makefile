ETCPACK_PATH ?= ../source

CPPFLAGS += -D_timeb=timeb -D_ftime=ftime
LDFLAGS += -static

.PHONY: all clean

all: etcpack

clean:
	$(RM) etcpack
	$(RM) *.o

etcpack: $(addprefix $(ETCPACK_PATH)/,etcpack.cxx etcdec.cxx image.cxx)
	$(LINK.cpp) $^ $(LOADLIBES) $(LDLIBS) -o $@
