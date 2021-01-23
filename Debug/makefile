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

BUILD_ARTIFACT_NAME := LinearPowerSupply_PS1401mA
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX := 
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME).$(BUILD_ARTIFACT_EXTENSION)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
LinearPowerSupply_PS1401mA.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
LinearPowerSupply_PS1401mA.list \

OBJCOPY_HEX += \
LinearPowerSupply_PS1401mA.hex \

OBJCOPY_BIN += \
LinearPowerSupply_PS1401mA.bin \


# All Target
all: main-build

# Main-build Target
main-build: LinearPowerSupply_PS1401mA.elf secondary-outputs

# Tool invocations
LinearPowerSupply_PS1401mA.elf: $(OBJS) $(USER_OBJS) C:\Users\Vasyl\Documents\GitHub\Linear-Power-Supply-PS1401-\STM32F100C8TX_FLASH.ld
	arm-none-eabi-gcc -o "LinearPowerSupply_PS1401mA.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\Vasyl\Documents\GitHub\Linear-Power-Supply-PS1401-\STM32F100C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="LinearPowerSupply_PS1401mA.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

LinearPowerSupply_PS1401mA.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "LinearPowerSupply_PS1401mA.list"
	@echo 'Finished building: $@'
	@echo ' '

LinearPowerSupply_PS1401mA.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "LinearPowerSupply_PS1401mA.hex"
	@echo 'Finished building: $@'
	@echo ' '

LinearPowerSupply_PS1401mA.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "LinearPowerSupply_PS1401mA.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents fail-specified-linker-script-missing warn-no-linker-script-specified
.SECONDARY:

-include ../makefile.targets
