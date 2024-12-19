CC = gcc
CFLAGS = -Wall -g -I/home/ice/mysyslog1/libmysyslog -I/home/ice/mysyslog1/libmysyslog-text -I/home/ice/mysyslog1/libmysyslog-json
LDFLAGS = -L/home/ice/mysyslog1/libmysyslog -L/home/ice/mysyslog1/libmysyslog-text -L/home/ice/mysyslog1/libmysyslog-json -lmysyslog -lmysyslog-text -lmysyslog-json

all: libmysyslog-daemon

mysyslog-daemon: libmysyslog-daemon.o
	$(CC) -o $@ $^ $(LDFLAGS)

mysyslog-daemon.o: libmysyslog-daemon.c
	$(CC) $(CFLAGS) -c $<

run: libmysyslog-daemon
	./libmysyslog-daemon

clean:
	rm -f libmysyslog-daemon *.o
