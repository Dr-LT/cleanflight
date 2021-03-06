# Board - AlienWii32

The AlienWii32 is actually in prototype stage only a few samples exist. There is some more field testing ongoing. The information below is preliminary and will be updated as needed.

Here are the hardware specifications:

- STM32F103CBT6 MCU
- MPU6050 accelerometer/gyro sensor unit
- 8x 4.2A brushed ESCs, integrated, to run the strongest micro motors
- extra-wide traces on the PCB, for maximum power throughput
- USB port, integrated
- (*) serial connection for external DSM2/DSMX sat receiver (e.g. Spektrum SAT, OrangeRx R100 or Lemon RX)
- alternatively PPM receiver connection (i.e. Deltang Rx31)
- ground and 3.3V for the receiver
- hardware bind plug for easy binding
- motor connections are at the corners for a clean look with reduced wiring
- dimensions: 29x33mm
- direct operation from an single cell lipoly battery

(*) Spektrum Compatible DSM2 satellites are supported out of the box. DSMX sat will work with DSM2 protocol with default settings (DSM2, 11bit, 11ms is preset). 

Deltang receivers in serial mode will work like any other Spektrum satellite receiver (10bit, 22ms) only the bind process will be different. 

The pin layout is very similar as the NAZE32 or the related clones (MW32, Flip32, etc.). The hardware bind pin is connected to pin 41 (PB5). The AlienWii32 firmware will be built with TARGET=NAZE and OPTIONS="AlienWii32". The firmware image will come with alternative default settings which will give the user a plug and play experience. There is no computer needed to get this into the air with an small Quadcopter. An preconfigured custom mixer for an Octocopter is part of the default settings to allow clean straight wiring with the AlienWii32. The mixer can be activated with "mixer custom" in the CLI. To use the AlienWii32 in an Hexa- or Octocopter or to do some more tuning additional configuration changes can be done as usual in the CLI or the Cleanflight configurator. 