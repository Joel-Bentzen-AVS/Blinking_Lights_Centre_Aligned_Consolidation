################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
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


BUILD_ARTIFACT_NAME := Blinking_Lights_Centre_Aligned_Consolidation
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Blinking_Lights_Centre_Aligned_Consolidation.elf \

MAP_FILES += \
Blinking_Lights_Centre_Aligned_Consolidation.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Blinking_Lights_Centre_Aligned_Consolidation.list \


# All Target
all: main-build

# Main-build Target
main-build: Blinking_Lights_Centre_Aligned_Consolidation.elf secondary-outputs

# Tool invocations
Blinking_Lights_Centre_Aligned_Consolidation.elf Blinking_Lights_Centre_Aligned_Consolidation.map: $(OBJS) $(USER_OBJS) C:\Users\JoelBentzen\STM32CubeIDE\workspace_1.10.1\Blinking_Lights_Centre_Aligned_Consolidation\STM32F746ZGTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "Blinking_Lights_Centre_Aligned_Consolidation.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"C:\Users\JoelBentzen\STM32CubeIDE\workspace_1.10.1\Blinking_Lights_Centre_Aligned_Consolidation\STM32F746ZGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Blinking_Lights_Centre_Aligned_Consolidation.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Blinking_Lights_Centre_Aligned_Consolidation.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Blinking_Lights_Centre_Aligned_Consolidation.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Blinking_Lights_Centre_Aligned_Consolidation.elf Blinking_Lights_Centre_Aligned_Consolidation.list Blinking_Lights_Centre_Aligned_Consolidation.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
