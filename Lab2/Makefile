BINARIES= \
	serial pthreads libdispatch

JOBS?=		100
WORK_PER_JOB?=	100

CC=		clang
CFLAGS=		-D JOBS=${JOBS} -D WORK_PER_JOB=${WORK_PER_JOB} \
		-Weverything -Wno-unused-parameter

# We don't need to link all of the following libraries for every program that
# we're going to compile, but there's no harm in attempting to do so
# (the linker will ignore any code it isn't looking for):
LDFLAGS=	-ldispatch -pthread -lBlocksRuntime -fblocks


all: ${BINARIES}

clean:
	rm -f ${BINARIES}

