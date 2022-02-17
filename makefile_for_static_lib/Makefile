VERSION     =
CC          =gcc
DEBUG   =
CFLAGS  =-Wall
AR   =ar
ARFLAGS     =rv
SOURCES   =$(wildcard *.c)
INCLUDES    =-I.
LIB_NAMES   =
LIB_PATH  =
OBJ         =$(patsubst %.c, %.o, $(SOURCES))
TARGET      =libfun_a

#使用ar命令将目标文件.o链接成静态库文件.a 
#静态库文件固定命名格式为libxxx.a
$(TARGET):$(OBJ)
	@mkdir -p output
	$(AR) $(ARFLAGS) output/$(TARGET)$(VERSION).a $(OBJ)
	@rm -rf $(OBJ)

#compile
%.o: %.c
	$(CC) $(INCLUDES) $(DEBUG) -c $(CFLAGS) $< -o $@
  
.PHONY:clean
clean:
	@echo "Remove linked and compiled files......"
	rm -rf $(OBJ) $(TARGET) output 