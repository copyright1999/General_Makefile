VERSION  =1.00
CC   =gcc

#-D是标识 后面是宏
DEBUG   =-DUSE_DEBUG

#编译选项 可以指定编译条件，如显示警告（-Wall），优化等级（-O）
CFLAGS  =-Wall

SOURCES   =$(wildcard ./source/*.c)
INCLUDES   =-I./include

#静态库libxxx.a  动态库libxxx.so 指定库文件名称只需要写xxx部分
LIB_NAMES  =-lfun_a -lfun_so

LIB_PATH  =-L./lib
OBJ   =$(patsubst %.c, %.o, $(SOURCES))
TARGET  =app

#links
$(TARGET):$(OBJ)
	@mkdir -p output
	$(CC) $(OBJ) $(LIB_PATH) $(LIB_NAMES) -o output/$(TARGET)$(VERSION)
	@rm -rf $(OBJ)
 
#编译
%.o: %.c
	$(CC) $(INCLUDES) $(DEBUG) -c $(CFLAGS) $< -o $@


.PHONY:clean
clean:
	@echo "Remove linked and compiled files......"
	rm -rf $(OBJ) $(TARGET) output 
