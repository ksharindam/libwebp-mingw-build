
CC = gcc
CXX = g++
CFLAGS = -Wall -O2 -fPIC -DPIC -DHAVE_CONFIG_H
CXXFLAGS = -Wall -O2 -std=c++11
INCLUDES = -I.. -Iwebp
LFLAGS = -shared
LIBS = -lm -pthread

BUILD_DIR = build
SOURCES = $(wildcard *.c)
OBJS = $(BUILD_DIR)/*.o

all:
	$(MAKE) -C dec
	$(MAKE) -C enc
	$(MAKE) -C dsp 
	$(MAKE) -C utils 
	ar rcs libwebp.a ${OBJS}
	${CC} ${LFLAGS} -o webp.dll ${OBJS} ${LIBS}

clean:
	rm -f $(BUILD_DIR)/*.o

# c
$(BUILD_DIR)/%.o: %.c
#	@mkdir -p $(@D)
	${CC} -c ${CFLAGS} ${INCLUDES} $< -o $@

# c++
$(BUILD_DIR)/%.o: %.cpp
#	@mkdir -p $(@D)
	${CXX} -c ${CXXFLAGS} ${INCLUDES} $< -o $@


