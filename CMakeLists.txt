add_executable(thor
        thor.c
	misc.c
        )

# pull in common dependencies
target_link_libraries(thor pico_stdlib hardware_spi hardware_i2c hardware_adc)

# create map/bin/hex file etc.
pico_add_extra_outputs(thor)

# add url via pico_set_program_url
example_auto_set_url(thor)

