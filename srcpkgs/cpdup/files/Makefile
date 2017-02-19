CC ?= cc
OBJS = cpdup.o fsmid.o hclink.o hcproto.o misc.o compat_linux.o

CFLAGS += -D__cpdup_unused="__attribute__ ((unused))" -D_GNU_SOURCE -D__USE_FILE_OFFSET64 -DNOMD5
CFLAGS += -DUSE_PTHREADS=1 -pthread

all: $(OBJS)
	$(CC) $(CFLAGS) $(LDFLAGS) $(OBJS) -o cpdup

.c.o:
	$(CC) $(CFLAGS) -c -o $@ $<
