################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: 3D-Cube.axf

# Tool invocations
3D-Cube.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -Xlinker -Map="3D-Cube.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -mcpu=cortex-m3 -mthumb -T "3D-Cube_Release.ld" -o "3D-Cube.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) 3D-Cube.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "3D-Cube.axf"; # arm-none-eabi-objcopy -v -O binary "3D-Cube.axf" "3D-Cube.bin" ; # checksum -p LPC1769 -d "3D-Cube.bin";
	-@echo ' '

.PHONY: all clean dependents post-build

-include ../makefile.targets
