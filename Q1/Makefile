obj-m := hello.o
KDIR = /lib/modules/$(shell uname -r)/build
PWD = $(shell pwd)

default:
	make -C $(KDIR) M=$(PWD) modules
	gcc write.c -o write
	gcc read.c -o read
	gcc ioctl.c -o ioctl
clean:
	make -C $(KDIR) M=$(PWD) clean
	rm write read ioctl
