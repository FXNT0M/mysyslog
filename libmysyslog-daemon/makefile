CC = gcc
CFLAGS = -Wall -g -I/home/fxnt0m/mysyslog1/libmysyslog -I/home/fxnt0m/mysyslog1/libmysyslog-text -I/home/fxnt0m/mysyslog1/libmysyslog-json
LDFLAGS = -L/home/fxnt0m/mysyslog1/libmysyslog -L/home/fxnt0m/mysyslog1/libmysyslog-text -L/home/fxnt0m/mysyslog1/libmysyslog-json -lmysyslog -lmysyslog-text -lmysyslog-json
all: libmysyslog-daemon

mysyslog-daemon: libmysyslog-daemon.o
	$(CC) -o $@ $^ $(LDFLAGS)

mysyslog-daemon.o: libmysyslog-daemon.c
	$(CC) $(CFLAGS) -c $<

run: libmysyslog-daemon
	./libmysyslog-daemon

clean:
	rm -f libmysyslog-daemon *.o
