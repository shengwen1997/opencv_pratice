#################################################################
EXECUTABLE=video_capture

#################################################################
#compiler
CC=g++

#################################################################
#include files
CFLAGS+=-I/usr/local/include/
CFLAGS=`pkg-config opencv --cflags` `pkg-config opencv --libs`
CFLAGS+=-lraspicam_cv -lraspicam

LDFLAGS:=

#################################################################
#compile all c++ files in dir
SRC=$(wildcard *.cpp)

#################################################################
OUTPUT=./output

all:$(EXECUTABLE)

$(EXECUTABLE):$(SRC)
	mkdir -p $(OUTPUT)
	$(CC) $< $(LDFLAGS) $(CFLAGS) -o $@

clean:
	rm -rf $(EXECUTABLE) $(OUTPUT)
#################################################################
