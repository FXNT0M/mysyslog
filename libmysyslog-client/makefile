CC = gcc
CFLAGS = -Wall -g -I/home/fxnt0m/mysyslog1/libmysyslog -I/home/fxnt0m/mysyslog1/libmysyslog-text -I/home/fxnt0m/mysyslog1/libmysyslog-json
LDFLAGS = -L/home/fxnt0m/mysyslog1/libmysyslog -L/home/fxnt0m/mysyslog1/libmysyslog-text -L/home/fxnt0m/mysyslog1/libmysyslog-json -lmysyslog -lmysyslog-text -lmysyslog-json

all: libmysyslog-client

mysyslog-client: libmysyslog-client.o
	$(CC) -o $@ $^ $(LDFLAGS)

mysyslog-client.o: libmysyslog-client.c
	$(CC) $(CFLAGS) -c $<

run: libmysyslog-client
	./libmysyslog-client

clean:
	rm -f libmysyslog-client *.o
