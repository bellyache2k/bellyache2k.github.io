


C hello world

```c
int main(void) {

    printf("Hello world\n");

    return 0;
}
```



a simple example of Makefile:

```make
CC = gcc
CFLAGS = -Wall -Wextra -Werror=declaration-after-statement -Wunused-but-set-variable -pedantic
CFLAGS += -g
#CLFAGS += -DNDEBUG
#CFLAGS += -O2
TARGET = a.out
SRCS = main.c cm.c
OBJS = $(SRCS:.c=.o)
 
$(TARGET): $(OBJS)
    $(CC) $(CFLAGS) -o $(TARGET) $(OBJS)
 
%.o: %.c
    $(CC) $(CFLAGS) -c $< -o $@
 
.PHONY: clean

clean:
    rm  $(OBJS) $(TARGET)
```

