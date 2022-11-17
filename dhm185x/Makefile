CC := avr-gcc
CFLAGS := -mmcu=attiny26 -Os -Wall
LDFLAGS :=
OBJS := main.o

all: dhm185x.bin

clean:
	rm -f $(OBJS) dhm185x dhm185x.bin

dhm185x: $(OBJS)
	$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^

dhm185x.bin: dhm185x
	avr-objcopy -O binary dhm185x dhm185x.bin
