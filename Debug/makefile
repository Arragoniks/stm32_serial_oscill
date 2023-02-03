################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include USB_DEVICE/Target/subdir.mk
-include USB_DEVICE/App/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := BluePill_USB_Oscill
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
BluePill_USB_Oscill.elf \

MAP_FILES += \
BluePill_USB_Oscill.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
BluePill_USB_Oscill.list \


# All Target
all: main-build

# Main-build Target
main-build: BluePill_USB_Oscill.elf secondary-outputs

# Tool invocations
BluePill_USB_Oscill.elf BluePill_USB_Oscill.map: $(OBJS) $(USER_OBJS) /home/komputator/STM32CubeIDE/workspace_1.11.0/BluePill_USB_Oscill/STM32F103C8TX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "BluePill_USB_Oscill.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/komputator/STM32CubeIDE/workspace_1.11.0/BluePill_USB_Oscill/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="BluePill_USB_Oscill.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

BluePill_USB_Oscill.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "BluePill_USB_Oscill.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) BluePill_USB_Oscill.elf BluePill_USB_Oscill.list BluePill_USB_Oscill.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
