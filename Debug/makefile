################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
DEVZONE_SX1278.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
DEVZONE_SX1278.list \

OBJCOPY_BIN += \
DEVZONE_SX1278.bin \


# All Target
all: DEVZONE_SX1278.elf secondary-outputs

# Tool invocations
DEVZONE_SX1278.elf: $(OBJS) $(USER_OBJS) E:\STM32\STM32\ workspace\ of\ Bien\DEVZONE_SX1278\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "DEVZONE_SX1278.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"E:\STM32\STM32 workspace of Bien\DEVZONE_SX1278\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="DEVZONE_SX1278.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

DEVZONE_SX1278.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "DEVZONE_SX1278.list"
	@echo 'Finished building: $@'
	@echo ' '

DEVZONE_SX1278.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "DEVZONE_SX1278.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
