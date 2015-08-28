obj-m := hello.o

KDIR  := /lib/modules/$(shell uname -r)/build
PWD   := $(shell pwd)

CLEAN_FILES += .cache.mk .hello.ko.cmd .hello.mod.o.cmd \
		  .hello.o.cmd Module.symvers hello.ko hello.mod.c \
		  hello.mod.o hello.o modules.order

CLEAN_DIRS += .tmp_versions

default:
	$(MAKE) -C $(KDIR) M=$(PWD) modules

.phony: clean

clean:
	$(RM) -r $(CLEAN_DIRS)
	$(RM) $(CLEAN_FILES)
