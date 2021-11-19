
CC = gcc
CXX = g++
CFLAGS = -Wall -O2 -fPIC -DPIC -DHAVE_CONFIG_H -pthread
CXXFLAGS = -Wall -O2 -std=c++11
INCLUDES = -I../.. -I../webp
LFLAGS = -s -shared
LIBS = -lm

BUILD_DIR = ../build
SOURCES = $(wildcard *.c)
OBJS = $(SOURCES:%.c=$(BUILD_DIR)/%.o)

all: ${OBJS}

clean:
	rm -f $(BUILD_DIR)/*.o

# c
$(BUILD_DIR)/%.o: %.c
#	@mkdir -p $(@D)
	${CC} -c ${CFLAGS} ${INCLUDES} $< -o $@

# c++
$(BUILD_DIR)/%.o: %.cpp
#	@mkdir -p $(@D)
	${CXX} -c ${CXXFLAGS} ${INCLUDES} -c $< -o $@


