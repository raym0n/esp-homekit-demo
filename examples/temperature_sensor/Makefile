PROGRAM = temperature_sensor

EXTRA_COMPONENTS = \
	extras/dht \
	extras/http-parser \
	$(abspath ../../components/wolfssl) \
	$(abspath ../../components/cJSON) \
	$(abspath ../../components/homekit)

# DHT11 sensor pin
SENSOR_PIN = 4

FLASH_SIZE = 32

EXTRA_CFLAGS += -I../.. -DHOMEKIT_SHORT_APPLE_UUIDS -DSENSOR_PIN=$(SENSOR_PIN)

include $(SDK_PATH)/common.mk

monitor:
	$(FILTEROUTPUT) --port $(ESPPORT) --baud 115200 --elf $(PROGRAM_OUT)
