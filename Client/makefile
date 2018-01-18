CFLAGS:= -c -Wall -Weffc++ -g -std=c++11 -Iinclude
LDFLAGS:= -lboost_system -lboost_thread

all: BBclient
	g++ bin/connectionHandler.o bin/client.o bin/task.o $(LDFLAGS) -o bin/BBclient

BBclient: bin/connectionHandler.o bin/client.o bin/task.o

bin/connectionHandler.o: src/ConnectionHandler.cpp
	g++ $(CFLAGS) -o bin/connectionHandler.o src/ConnectionHandler.cpp

bin/client.o: src/EchoClient.cpp
	g++ $(CFLAGS) src/EchoClient.cpp -o bin/client.o

bin/task.o: src/Task.cpp
	g++ $(CFLAGS) src/Task.cpp -o bin/task.o
.PHONY: clean
clean:
	rm -f bin/*