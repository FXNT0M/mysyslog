CC = gcc
CFLAGS = -Wall -g -I/home/fxnt0m/mysyslog/libmysyslog -I/home/fxnt0m/mysyslog/libmysyslog-text -I/home/fxnt0m/mysyslog/libmysyslog-json
LDFLAGS = -L/home/fxnt0m/mysyslog/libmysyslog -L/home/fxnt0m/mysyslog/libmysyslog-text -L/home/fxnt0m/mysyslog/libmysyslog-json -lmysyslog -lmysyslog-text -lmysyslog-json
all: libmysyslog-daemon

libmysyslog-daemon: libmysyslog-daemon.o
	$(CC) -o $@ $^ $(LDFLAGS)

libmysyslog-daemon.o: libmysyslog-daemon.c
	$(CC) $(CFLAGS) -c $<

run: libmysyslog-daemon
	./libmysyslog-daemon

clean:
	rm -f libmysyslog-daemon *.o
