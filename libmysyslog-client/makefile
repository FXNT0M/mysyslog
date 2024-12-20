CC = gcc
CFLAGS = -Wall -g -I/home/fxnt0m/mysyslog/libmysyslog -I/home/fxnt0m/mysyslog/libmysyslog-text -I/home/fxnt0m/mysyslog/libmysyslog-json
LDFLAGS = -L/home/fxnt0m/mysyslog/libmysyslog -L/home/fxnt0m/mysyslog/libmysyslog-text -L/home/fxnt0m/mysyslog/libmysyslog-json -lmysyslog -lmysyslog-text -lmysyslog-json

all: libmysyslog-client

libmysyslog-client: libmysyslog-client.o
	$(CC) -o $@ $^ $(LDFLAGS)

libmysyslog-client.o: libmysyslog-client.c
	$(CC) $(CFLAGS) -c $<

run: libmysyslog-client
	./libmysyslog-client

clean:
	rm -f libmysyslog-client *.o
