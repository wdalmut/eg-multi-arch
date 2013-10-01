CC=/usr/bin/gcc
AR=/usr/bin/ar

CFLAGS=-g3 -Wall

BUILD_DIR=../../build/arch2

all: init
	${CC} ${CFLAGS} -c -o ${BUILD_DIR}/base.o base.c
	${AR} -rsc ${BUILD_DIR}/arch2.a ${BUILD_DIR}/base.o

init:
	mkdir -p ${BUILD_DIR}

clean:
	rm ${BUILD_DIR}/base.o
	rm ${BUILD_DIR}/arch2.a

