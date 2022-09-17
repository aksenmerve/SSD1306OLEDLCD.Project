################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
SSD136_LCD_Example.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
SSD136_LCD_Example.list \

OBJCOPY_BIN += \
SSD136_LCD_Example.bin \


# All Target
all: SSD136_LCD_Example.elf secondary-outputs

# Tool invocations
SSD136_LCD_Example.elf: $(OBJS) $(USER_OBJS) C:\Users\voyvoda\STM32CubeIDE\workspace_1.3.0\SSD136_LCD_Example\STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "SSD136_LCD_Example.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\voyvoda\STM32CubeIDE\workspace_1.3.0\SSD136_LCD_Example\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="SSD136_LCD_Example.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

SSD136_LCD_Example.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "SSD136_LCD_Example.list"
	@echo 'Finished building: $@'
	@echo ' '

SSD136_LCD_Example.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "SSD136_LCD_Example.bin"
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
