AUTOMAKE_OPTIONS = foreign

INITIAL_TARGETS = PrintfMsg.class PrintfMsg.java

ROOT = ../../..
include $(ROOT)/Makefile.include

PRINTF_H = $(TINYOS_OS_DIR)/lib/printf/printf.h
TFLAGS = -I$(TINYOS_OS_DIR)/types -I$(TINYOS_OS_DIR)/platforms/null -I$(TINYOS_OS_DIR)/lib/serial -DNEW_PRINTF_SEMANTICS
NFLAGS = -fnesc-gcc=$(CC)

PrintfMsg.java: $(PRINTF_H)
	nescc-mig $(NFLAGS) java $(CFLAGS) $(TFLAGS) -java-classname=net.tinyos.tools.PrintfMsg $(PRINTF_H) printf_msg -o $@
