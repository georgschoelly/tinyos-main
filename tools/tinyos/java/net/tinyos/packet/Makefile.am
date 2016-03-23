AUTOMAKE_OPTIONS = foreign

INITIAL_TARGETS = Serial.class Serial.java

ROOT = ../../..
include $(ROOT)/Makefile.include

SERIAL_H = $(TINYOS_OS_DIR)/lib/serial/Serial.h
TFLAGS = -I$(TINYOS_OS_DIR)/lib/serial -I$(TINYOS_OS_DIR)/types
NFLAGS = -fnesc-gcc=$(CC)

Serial.java: $(SERIAL_H)
	nescc-ncg $(NFLAGS) -o $@ $(TFLAGS) -java-classname=net.tinyos.packet.Serial java $(SERIAL_H) Serial.h
