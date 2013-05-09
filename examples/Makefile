
PADIR := ..

EXAMPLESRC := $(wildcard ./*.c)
EXAMPLESRC := $(filter-out ./paex_wmme%.c, $(EXAMPLESRC))
EXAMPLESRC := $(filter-out ./paex_record_file.c, $(EXAMPLESRC))

EXAMPLEOBJ := $(EXAMPLESRC:.c=.o)

PALIB := $(PADIR)/lib/libportaudio.a

CC := clang

CINCLUDES := -I$(PADIR)/include -I$(PADIR)/src/common -lm

APPLEAUDIO := -framework CoreAudio -framework AudioToolbox -framework AudioUnit -framework CoreServices

#CFLAGS = -Wall -g -O0 -Weverything -Wno-unused-parameter -Wno-padded -Wno-weak-vtables
CFLAGS = -Wall -g -O0

all: examples

examples: $(EXAMPLEOBJ)

%.o: %.c
	 $(CC) $(CINCLUDES) $(CFLAGS) $(PALIB) $(APPLEAUDIO) $< -o $@

clean:
	rm -rf *.o *.dSYM
