KDIR := ~/linux-rpi
ARM := ARCH=arm CROSS_COMPILE=arm-linux-gnueabi-
PWD :=$(shell pwd)

obj-m := challenge.o

default:
	$(MAKE) -C $(KDIR) M=$(PWD) $(ARM) modules

copy:
	scp challenge.ko mknod.sh challenge_app pi@10.10.10.13:~/


clean:
	$(MAKE) -C $(KDIR) M=$(PWD) $(ARM) clean

