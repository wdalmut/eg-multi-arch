RM=/bin/rm
CC=/usr/bin/gcc
OUTPUT_PATH=../build
APP=${OUTPUT_PATH}/app
CFLAGS=-g -Wall -O3
MAKE=/usr/bin/make

all: a1

init:
	mkdir -p ${OUTPUT_PATH}
	$(MAKE) -C arch1 all
	${MAKE} -C arch2 all

a1: init
	${CC} ${CFLAGS} main.c -Iarch1 ${OUTPUT_PATH}/arch1/arch1.a -o ${APP}

a2: init
	${CC} ${CFLAGS} main.c -Iarch2 ${OUTPUT_PATH}/arch2/arch2.a -o ${APP}

clean:
	${MAKE} -C arch1 clean
	${MAKE} -C arch2 clean
	${RM} -rf ${OUTPUT_PATH}

