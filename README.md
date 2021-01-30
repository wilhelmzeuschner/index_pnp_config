# index_pnp_config
machine.xml file ([openPNP](https://github.com/openpnp/openpnp) config for the [index PNP project](https://github.com/sphawes/index))


## Information:

### Driver (Interface to the Board via UART):
Configured for 250000 baud. Changed from 115200 to have higher speeds. This setting needs to be set according to the firmware.
COM port is specific to the individual setup.

### Outputs:
Mosfets 1 to 4 can be turned on. Mosfet 1 is assigned to head 1 as the vacuum pump.
Mosfets 2 to 4 are actuators. They are treated as fans by Marlin.
Currently [M106](https://marlinfw.org/docs/gcode/M106.html) and [M107](https://marlinfw.org/docs/gcode/M107.html) commands are used to turn them on and off.
They are configured as binary outputs (though PWM should be possible too).

### Cameras:
The basics for two cameras (up and down) are set up. Details are missing.
This setting likely needs to be changed depending on the hardware setup.

