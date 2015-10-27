PROJECT=dlloader
CC=gcc -std=c++11 -g
SHARED_FLAG = -fPIC -shared
INC += -I../
SRCS = . ..
SOURCES = $(foreach d,$(SRCS),$(wildcard $(d)/*.cpp))
OBJS = $(patsubst %.cpp, %.o, $(SOURCES))

all : dlloader

$(PROJECT): $(OBJS)
	$(CC) -o $@ $(OBJS) -ldl -lstdc++
	@echo ""
	@echo "+--------------------------------------------+"
	@echo "|            Finish compilation              |"
	@echo "+--------------------------------------------+"
	@echo "|         Thanks using dlloader              |"
	@echo "|   copyright(c)Wang Yaofu  voipman@qq.com   |"
	@echo "+--------------------------------------------+"

clean:
	rm -rf *.o $(PROJECT)


%.o : %.cpp
	$(CC) $(INC) -c $< -o $@
%.o : %.c
	$(CC) $(INC) -c $< -o $@
%.o : %.cc
	$(CC) $(INC) -c $< -o $@
