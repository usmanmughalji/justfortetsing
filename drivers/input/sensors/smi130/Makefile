#
# Makefile for Bosch sensor driver.
#

obj-$(CONFIG_BOSCH_DRIVER_LOG_FUNC) += bs_log.o
obj-y += boschclass.o
ifeq ($(CONFIG_BOSCH_DRIVER_LOG_FUNC),y)
	EXTRA_CFLAGS += -DBOSCH_DRIVER_LOG_FUNC
endif

obj-y   += smi130_acc.o

ifeq ($(CONFIG_SENSORS_SMI_ACC2X2_ENABLE_INT1),y)
	EXTRA_CFLAGS += -DSMI_ACC2X2_ENABLE_INT1
endif

ifeq ($(CONFIG_BOSCH_SMI_ACC2X2_ENABLE_INT2),y)
	EXTRA_CFLAGS += -DSMI_ACC2X2_ENABLE_INT2
endif

obj-y    += smi130_gyro_driver.o smi130_gyro.o
EXTRA_CFLAGS += -DSMI_GYRO_USE_BASIC_I2C_FUNC

obj-y    += smi130_driver.o smi130.o
ifeq ($(CONFIG_SMI130_MAG_INTERFACE_SUPPORT),y)
		EXTRA_CFLAGS += -DSMI130_MAG_INTERFACE_SUPPORT
endif
ifeq ($(CONFIG_SENSORS_SMI130_ENABLE_INT1),y)
		EXTRA_CFLAGS += -DSMI130_ENABLE_INT1
endif

ifeq ($(CONFIG_SENSORS_SMI130_ENABLE_INT2),y)
		EXTRA_CFLAGS += -DSMI130_ENABLE_INT2
endif

obj-y  += smi130_i2c.o

EXTRA_CFLAGS += -DSMI_USE_BASIC_I2C_FUNC

obj-$(CONFIG_SENSORS_SMI130_SPI)  += smi130_spi.o
