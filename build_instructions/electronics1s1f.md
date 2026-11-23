# Electronics: Cytkit configuration 1S-1F

The Cytkit configuration 1S-1F uses entirely off-the shelf electronics to provide one channel of scatter and one channel of fluorescence. This configuration is primarily of use for education and technology development rather than as a useful spectral cytometer, of course. It may easily be adapted for alternative detectors and acquisition electronics. However, some skills in electronics are required to prepare cables and connectors, solder or crimp terminals, and choose power supplies.

![Cytkit 1s-1f fully assembled](images/build photos/20260530_180033 cytkit 1s-1f assembled.jpg)

## Mount FSC detector  {pagestep}

Attach the [Amplified photodiode (Thorlabs PDA10)](components/thorlabs_pda10.md){qty:1, cat:electronics1s1f} to the [PD module holder](printed/Amplified_PD_holder.md){qty:1, cat:printed1S1F} with an [M4 hex socket bolt 10 mm](mechanical/screws.yaml#m4x10_hex_socket){qty:1, cat:mechanics}. Attach the assembly to the main body with 2x [M3 self-tapping posi head screws 12 mm](mechanical/screws.yaml#self_tapping_m3x12_posi){qty:2, cat:mechanics}.

The Thorlabs PDA10 comes with a BNC socket to connect to the oscilloscope, and a power supply socket for its own power supply. You require a [BNC (Male) to BNC (Male) cable, 1 m](electronic/bnc_cable.md){qty:1, cat:electronics1s1f}.

![](images/build photos/1s1f/20261116-0419509610.jpg)

## Mount PMT detector {pagestep}

Attach the [Photomultiplier tube module (Hamamatsu H10732)](components/hamamatsu_H10732.md){qty:1, cat:electronics1s1f} to the [PMT mount](printed/PMT_mount.md){qty:1, cat:printed1S1F} with 4x  [M2 hex socket bolt 8 mm](mechanical/screws.yaml#m2x8_hex_socket){qty:4, cat:mechanics}.

The PMT module requires a stable +5V, 0 and -5V power supply. It provides a stable 1V reference voltage for creating a variable bias voltage using a 10k potentiometer from the reference to the 0V pin. With some soldering skills and a Stripboard, one can make stable power supply with 8 x NiMH AA cells (approx 1.2 V x 4 for each of the +5 and -5 referenced to zero). One can also use a linear mode laboratory power supply with two floating adjustable voltage sources, where the positive of one voltage source is connected to the negative of the other. Use a [SMA (Female) to BNC (Male) adapter](electronic/sma_bnc_adapter.md){qty:1, cat:electronics1s1f} to connect the module to the oscilloscope.

Separately, attach the [PMT mount base](printed/PMT_mount_base.md){qty:1, cat:printed1S1F} to the main body with 2x  [M3 countersunk posi-head 10 mm screws](mechanical/screws.yaml#self_tapping_m3x10_posi_head_countersunk){qty:2, cat:mechanics}. The PMT module can be located according to a pin in the linear array as shown. Place the module at the 4th pin which corresponds to the emission peak of PE.

![](images/build photos/1s1f/20261116-0420550820.jpg)
![](images/build photos/1s1f/20261116_162513.jpg)
![](images/build photos/1s1f/20261116_162553.jpg)
![](images/build photos/1s1f/20261116_173332.jpg)

## LED flash calibration tool {pagestep}

This optional tool allows the calibration of fluorescence detector signals by an LED flash. Take one [3mm F3 round white LED](electronic/f3_led.md){qty:1, cat:electronics1s1f} and solder a [16k resistor](electronic/16k_resistor.md){qty:1, cat:electronics1s1f} to one leg. Solder a cable to connect it to a signal generator. When mounted, a 5 V pulse has approximately the same brightness in the PE peak emission channel as the brightest peak of the [Spherotech 8-peak Rainbow Beads RCP-30-5A](test_materials/spherotech8peak.md).

![](images/build photos/1s1f/20261116_163339.jpg)
![](images/build photos/1s1f/20261116_163413.jpg)

## Sample pump stepper motor controller {pagestep}

The [Peristaltic pump for sample](fluidic/sample_pump.md){qty:1, cat:fluidics} uses a 2-coil 4-pin stepper motor with a JST SH1.0 female 4-pin connector. The Astute Devices Cytometry Electronics Set includes a connector board for this pump, but it is quite difficult to find an off-the-shelf JST SH1.0 male with a cable. Therefore the most practical solution to control it is to cut off the connector, solder 4 wires onto it and attach a Dupont 4-pin female plug, which attaches to the [Stepper motor controller board](electronic/stepper_controller.md){qty:1, cat:electronics1s1f}. 

![](images/build photos/1s1f/20261116_162642.jpg)
![](images/build photos/1s1f/20261116_162814.jpg)

## Sheath pump DC motor controller {pagestep}

Solder two wires onto the [Vacuum pump for sheath](fluidic/sheath_pump.md){qty:1, cat:fluidics} as shown. These can be screwed into the [Vacuum pump controller board](electronic/vacuum_pump_controller.md){qty:1, cat:electronics1s1f} as shown.

![](images/build photos/1s1f/20261116_162910.jpg)
![](images/build photos/1s1f/20261116_163029.jpg)


## Power supplies {pagestep}

The laser module, the sample pump and the sheath pump all require a 5 V power source. It is convenient to use a powered USB hub such as the one shown as a power supply, since each component can be individually switched. This requires 3 USB A power cables.

![](images/build photos/1s1f/20261116_163217.jpg)

## Camera {pagestep}

The [USB camera module](electronic/camera.md){qty:1, cat:electronics1s1f} comes with a JST SH1.0 5-pin to USB A connector. The camera mount and lens is described in the [optics assembly instructions](assemble_optics.md).

![](images/build photos/1s1f/20261116_172535.jpg)

## Connect detectors and controllers. 

Mount the detectors as shown below. The mounting of the pumps and laser is described under [fluidics](assemble_fluidics.md) and [optics](assemble_optics.md).

Connect the detectors to the oscilloscope. If you just want to see raw signals, you can use any oscilloscope. However, Honeychrome comes with a driver for a [Picoscope 5000 series](components/picoscope.md) oscilloscope, which is convenient to record and analyse cytometry data. Attach the FSC detector to Channel A and the fluorescence detector to Channel B. Connect the Picoscope's USB cable to your host PC.

![](images/build diagrams/optics/main body with optics - 1s1f annotated.png)
![](images/build photos/1s1f/20261116_210941.jpg)
![](images/build photos/1s1f/20261116_210842.jpg)
![](images/build photos/1s1f/20261116_211024.jpg)

Now proceed with the software set-up. 