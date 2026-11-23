# Fine alignment

If you are building the Cytkit configuration 2S14F, fine alignment should be done with the instrument cover on (laser enclosed and interlock enabled).

If you are building the Cytkit configuration 1S1F, do not place the instrument cover yet, as it must be off to access the FSC alignment.

## Flow alignment beads {pagestep}

To carry out fine alignment, you need [bright green fluorescent alignment beads](test_materials/alignment_beads.md){qty:1, cat:test_materials}. Dilute them to a reasonable concentration (say, 1e5 to 1e6 per mL) in a [5 mL flow cytometry test tube](test_materials/test_tube.md).

Flow them on your Cytkit as follows.

Switch on the sheath flow:

- for 1S1F configuration, power the pump directly with the power supply and motor controller;
- for 2S14F configuration, press the initialisation button in the acquisition widget.

Load the sample:

- for 1S1F configuration, control the stepper motor directly, flow at a low rate ~ 30 uL/min;
- for 2S14F configuration, press the start button in the acquisition widget; flow at 30 uL/min.

## Signal check {pagestep}

When the beads pass through the laser focus, they will emit an intense flash of fluorescent light. Set Honeychrome to trigger on fluorescence: Edit > Instrument Configuration. Set peak detection channel to B1 for Cytkit 1S1F; B4 for Cytkit 2S14F. Set peak detection threshold to 200 mV.

If coarse alignment was successful. In Honeychrome (View > Oscilloscope Viewer) you should see something like the following: a rising edge refreshing several times per second. If you do not, gradually increase your fluorescence detector's bias voltage, making sure that the baseline stays below 100 mV.

<video src="images/build photos/alignment/Screencast from 2026-11-19 12-27-01 alignment beads after coarse alignment in honeychrome.webm" controls width="640"></video>

For Cytkit 1S1F you can also do the same in the Picoscope software. 

<video src="images/build photos/alignment/Screencast from 2026-11-19 12-25-37 alignment beads after coarse alignment in picoscope.webm" controls width="640"></video>

If you don't see any signal like this, check the following:

- Is the sheath flowing? (See if fluid is dripping into waste bottle.)
- Is the sample flowing? (Can you hear the stepper motor / can you see its gears turning?)
- Did you wait long enough for the sample to fill the input tube? (For Cytkit 1S1F, this is about 10 seconds of fast flow on the sample pump. For Cytkit 2S14F it is managed automatically by pressing start in the acquisition widget.)
- Is the laser on, and are the detectors working? (You should see much higher background noise with the laser on than the laser off. In the oscilloscope, with subtract background unchecked, you should see a difference in the FSC level with laser on and off.)

If all the above are working but you still don't see signal, then coarse alignment was not close enough. Go back and check it.

## Align laser and fluorescence collection (fine) {pagestep}

While watching the oscilloscope, carefully adjust the following in order to make the flurorescence peak narrow in width (time), and bright in height (fluorescence amplitude). Ignore scatter for now. As the fluorescence peak height increases, lower your bias voltage to keep the peaks unsaturated.

1. x1 laser focus
1. theta laser focus
1. y1 laser focus
1. y2 condenser
1. x2 condenser

Your fluorescence peak should start to look like a clean Gaussian as shown below.

<video src="images/build photos/alignment/Screencast from 2026-11-19 14-34-08 alignment beads after align fine fl.webm" controls width="640"></video>

>i Tip: Make your adjustments carefully: before turning each lead screw, make a mental note of its position, so that you can return to it if you go to far and the signal disappears. 
>i 
>i Don't continue adjusting blindly if the signal disappears! Searching for the laser focus after losing it is like trying to fine a needle in a 5-dimensional haystack!

## Align FSC collection {pagestep}

After aligning fluorescence collection, align scatter (FSC and SSC). Keep the trigger on fluorescence for now.

In the oscilloscope, uncheck "subtract background". Adjust y3 FSC until the FSC baseline is minimised. (Note the channel is inverted: minimising baseline here corresponds to putting the FSC detector in the brightest part of the beam.) You should now see peaks in FSC. If you reduce the flow rate to 10 uL/min they should become very regular in height.

If FSC is not regular in height, check the following:

- Do you have bubbles / outgassing in your sheath fluid? (Are there bubbles in the sheath input line? If so, leave the sheath overnight for the gas to equilibrate, or pre-warm the sheath to ~ 40 C to drive out excess gas, and let it cool before using.)
- Do you have a clog / debris in your flow cell? Try flowing cytometry cleaning agents before flowing the beads again.

<video src="images/build photos/alignment/Screencast from 2026-11-19 14-41-05 alignment beads after align fine fsc trig fl.webm" controls width="640"></video>

You should now be able to trigger on FSC (Instrument Settings > Peak Detection Channel). Set threshold to 150 mV for Cytkit 1S1F or 50 mV for Cytkit 2S14F.

<video src="images/build photos/alignment/Screencast from 2026-11-19 14-45-04 alignment beads after align fine fsc.webm" controls width="640"></video>

If you are building the Cytkit configuration 1S1F, you may now place the instrument cover. (You will have to disconnect the FSC leads and tuck away any other leads before placing the cover on. This is not necessary for the Cytkit configuration 2S14F where the leads are all enclosed.)

## Align SSC collection {pagestep}

To align SSC (Cytkit 2S14F), adjust z SSC until the SSC peak height is maximised in the oscilloscope. 

Your Cytkit is now set up! Move on to test it.