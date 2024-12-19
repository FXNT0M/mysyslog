CC = gcc
CFLAGS = -Wall -g -I/home/ice/mysyslog1/libmysyslog -I/home/ice/mysyslog1/libmysyslog-text -I/home/ice/mysyslog1/libmysyslog-json
LDFLAGS = -L/home/ice/mysyslog1/libmysyslog -L/home/ice/mysyslog1/libmysyslog-text -L/home/ice/mysyslog1/libmysyslog-json -lmysyslog -lmysyslog-text -lmysyslog-json

all: libmysyslog-client

mysyslog-client: libmysyslog-client.o
	$(CC) -o $@ $^ $(LDFLAGS)

mysyslog-client.o: libmysyslog-client.c
	$(CC) $(CFLAGS) -c $<

run: libmysyslog-client
	./libmysyslog-client

clean:
	rm -f libmysyslog-client *.o
