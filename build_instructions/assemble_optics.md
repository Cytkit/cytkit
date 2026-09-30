# Assemble the optics

>! **Caution** 
>!
>! Wear gloves to handle optics! The human hand is never clean enough to touch a lens or filter. Don't contaminate them with fingerprints.
>! 
>! You can use plastic tweezers to handle the glass optical elements. Don't use metal tweezers as they risk scratching or chipping the glass.
>! 

## Assemble laser module  {pagestep}
First cut of the brims and support tab of the printed [Laser holder](printed/laser_holder.md) as shown. 

Second, attach the [Laser heatsink](optical/laser_heatsink.md) to the laser holder with 4x [M3 self-tapping posi head screws 10 mm](mechanical/screws.yaml#self_tapping_m3x10_posi){qty:4, cat:mechanics}

Third, screw the M9 mounted [Laser collimating lens](optical/laser_collimating_lens.md){qty:1, cat:optics} into the internal thread at the front of the laser module. About 2 mm of the threaded mount should be poking out from the laser module.

Fourth, insert the [Laser collimating lens lock nut adjustment tool (short)](printed/lock_nut_tool_short.md){qty:1, cat:printed_resin} through the [Laser collimating lens lock nut](printed/lock_nut.md){qty:1, cat:printed_resin} so that its two teeth stick out on the side facing the mounted laser collimating lens. 

Fifth, using the tool to stop the laser collimating lens from rotating, rotate the lock nut onto the mounted laser collimating lens until it gently locks against the body of the laser module, as shown.

Sixth, insert the laser module into the laser heatsink and tighten the two retaining screws gently.

Seventh, attach the laser module to the [Main body](printed/main_body.md) with 2x [M3 self-tapping posi head screws 16 mm](mechanical/screws.yaml#self_tapping_m3x10_posi){qty:4, cat:mechanics} at the front of the module, and 1x [M3 self-tapping hex socket cap screws 25 mm](mechanical/screws.yaml#self_tapping_m3x25_hex_socket){qty:1, cat:mechanics} with 1x [Stainless steel compression springs, 0.5 mm wire, 20 mm length, 6 mm diameter](mechanical/springs_20x6x0.5mm.md){qty:1, cat:mechanics} at the adjustment arm at the back of the module.

![](images/build diagrams/optics/laser assembly annotated.png)
![](images/build photos/20260530_150922 assemble laser collimating lens.jpg)
![](images/build photos/20260530_151240 assembled laser module.jpg)
![](images/build photos/20260530_151545 attach laser assembly.jpg)

## Assemble and mount beam shaping assembly  {pagestep}

The beam shaping assembly comprises three optical components: [Laser focus lens spherical](optical/laser_focus_lens_spherical.md){qty:1, cat:optics},  [Laser focus lens cylindrical](optical/laser_focus_lens_cylindrical.md){qty:1, cat:optics} and [Band pass dichroic filter](optical/band_pass_dichroic.md){qty:1, cat:optics} which are all mounted onto the single [Focusing lens holder](printed/foc_lens_holder.md){qty:1, cat:printed}. The holder has a non zero angle of the bandpass dichroic filter to reduce reflections into the laser diode.

Firstly insert the components carefully into the focusing lens holder as shown. 

Secondly, attach the beam shaping assembly to the [Main body](printed/main_body.md) with 1x [M3 self-tapping posi head screws 8 mm](mechanical/screws.yaml#self_tapping_m3x8_posi){qty:1, cat:mechanics}. The screw attaches to the raised screw hole in the main body's laser alignment XY flexure stage through the slot on the focusing lens holder. Take care when tightening the screw: make it just tight enough to stop the holder moving, not so tight that it damages the 3D printed layers on the XY stage's screw hole.

![](images/build diagrams/optics/focus lens holder assembly annotated.png)
![](images/build diagrams/optics/beam shaping assm to xy stage.png)
![](images/build photos/20260530_150506 beam shaping assembly.jpg)
![](images/build photos/20260530_150647 beam shaping assembly 2.jpg)

## Insert condensing lens {pagestep}

First insert the [Condensing lens](optical/condensing_lens.md){qty:1, cat:optics} into the [Condensing lens holder](printed/condensing_lens_holder.md){qty:1, cat:printed}.

Second screw this assembly only the main body's condensing lens XY flexure stage using 1x [M3 self-tapping posi head screws 8 mm](mechanical/screws.yaml#self_tapping_m3x8_posi){qty:1, cat:mechanics}.

![](images/build diagrams/optics/condensing lens assembly.png)
![](images/build photos/20260530_145457 aspherical condenser lens assm.jpg)
![](images/build diagrams/optics/condensing lens to main body.png)

## Insert cylindrical correction lens (only if using cylindrical capillary) {pagestep}

>i Ignore this step if using a square-section cuvette.

First insert the [Cylindrical correction lens](optical/cylindrical_correction_lens.md){qty:1, cat:optics} into its [Correction cylindrical lens holder](printed/correction_cyl_lens_holder.md){qty:1, cat:printed}.

Second screw onto the main body (fitting on the screwhole in the arm of the condensing lens XY flexure stage) with 1x [M3 self-tapping posi head screws 8 mm](mechanical/screws.yaml#self_tapping_m3x8_posi){qty:1, cat:mechanics}.

![](images/build diagrams/optics/correction cylindrical assembly.png)
![](images/build diagrams/optics/correction cyl to main body assm.png)


## Insert neutral density filter {pagestep}

First insert the [Neutral density filter](optical/nd_filter.md){qty:1, cat:optics} into the [ND filter holder for FSC](printed/nd_filter_holder.md){qty:1, cat:printed2S14F}.

Second screw the holder into the main body on the screw hole opposite the laser as shown, with  1x [M3 self-tapping posi head screws 12 mm](mechanical/screws.yaml#self_tapping_m3x12_posi){qty:1, cat:mechanics}.

![](images/build diagrams/optics/nd filter assembly.png)
![](images/build diagrams/optics/attach nd filter assm.png)



## Insert dichroic and/or coloured glass filters  {pagestep}

>i Here you have options depending on your budget. High performing spectral filters cost money. To achieve good sensitivity, one needs a high optical density removal of the laser light at 488 nm (ideally OD > 6) while letting through light in the band of sensitivity of the detectors, say 500 to 900 nm. 
>i
>i The cheap option involves stacking a low-cost dichroic filter with a coloured glass filter. For less than USD 50 from Far-East suppliers (or about USD 200 from the major optics catalogue companies), you can have filters that achieve good sensitivity from about 520 nm upwards. However this loses the difference between the blue emitting fluorophores such as FITC, GFP and BB515.
>i
>i For higher budgets, you can have a single dichroic filter here that achieves high blocking of the laser light while being substantially transparent at 500 nm and upwards. The well known quality suppliers are listed [here](optical/dichroic_longpass.md). 

The [Dichroic longpass filter at 0 degrees](optical/dichroic_longpass.md){qty:1, cat:optics} should have its coated surface facing the light source. Establish which surface this is by inspecting the edges of the filter with a loupe.

Insert the dichroic longpass filter and / or [Coloured glass longpass filter](optical/coloured_glass_longpass.md){qty:1, cat:optics} into their respective holders. Depending on size, the following filter holders are available:

- [Circular filter holder (34mm diameter)](printed/circular_filter_holder_34mm_diameter.md){qty:1, cat:printed}
- [Circular filter holder (25mm diameter)](printed/circular_filter_holder_25mm_diameter.md){qty:1, cat:printed}
- [Circular filter holder (15mm diameter)](printed/circular_filter_holder_15mm_diameter.md){qty:1, cat:printed}
- [Rectangular filter holder (25.5x26mm)](printed/rectangular_filter_holder.md){qty:1, cat:printed}

Then attach each filter holder to the main body as shown using 1x [M3 self-tapping posi head screws 12 mm](mechanical/screws.yaml#self_tapping_m3x12_posi){qty:1, cat:mechanics}.

>i If using a combination of a dichroic filter and a coloured glass filter, the dichroic should always be before the coloured glass in the optical train, to minimise the background fluorescence caused by the laser light in the coloured glass filter.

![](images/build diagrams/optics/filter assembly.png)
![](images/build diagrams/optics/attach filter holders to main body.png)


## Insert SSC focusing lens  {pagestep}

First insert the [SSC focusing lens](optical/ssc_focusing_lens.md){qty:1, cat:optics} into the [SSC focusing lens holder](printed/ssc_focus_lens_holder.md){qty:1, cat:printed}.

Second attach the SSC lens holder to the main body as shown with 1x [M3 self-tapping posi head screws 12 mm](mechanical/screws.yaml#self_tapping_m3x12_posi){qty:1, cat:mechanics}. The space here is very limited for fingers, therefore it is recommended to use plastic tweezers for this step.

![](images/build diagrams/optics/ssc lens assembly.png)
![](images/build diagrams/optics/attach ssc to main body.png)

## Insert grating  {pagestep}

First insert the [Blazed reflection grating](optical/blazed_reflection_grating.md){qty:1, cat:optics} in the [Grating holder](printed/grating_holder.md){qty:1, cat:printed}. Make sure the arrow showing the blaze direction is pointing as shown.

Second attach the grating holder to the main body using 2x [M3 self-tapping posi head screws 12 mm](mechanical/screws.yaml#self_tapping_m3x12_posi){qty:2, cat:mechanics} as shown.

![](images/build diagrams/optics/grating assembly.png)
![](images/build diagrams/optics/attach grating.png)

## Insert spectrum focusing lens {pagestep}

First insert the [Spectrum focusing lens](optical/spectrum_focusing_lens.md){qty:1, cat:optics} in the [Spectrum focusing lens holder](printed/spectrum_focus_lens_holder.md){qty:1, cat:printed}.

Then attach the holder to the main body using 4x [M3 self-tapping posi head screws 12 mm](mechanical/screws.yaml#self_tapping_m3x12_posi){qty:4, cat:mechanics} as shown.

![](images/build diagrams/optics/spectrum focusing lens to holder.png)
![](images/build diagrams/optics/attach spectrum focus lens.png)


## Insert dichroic beamsplitter  {pagestep}

>! The dichroic beamsplitter (longpass filter at 45 degrees) goes straight into a holder which is part of the main body. Therefore be extremely careful not to break the holder, otherwise you will have to print the main body again!

First establish which surface of the [Dichroic longpass filter at 45 degrees (beamsplitter)](optical/dichroic_longpass_45.md){qty:1, cat:optics} has the coating. You can do this by inspecting the corners of the glass with a loupe. 

With the coated surface facing the condensing lens, insert the beamsplitter into the slots in the main body. Tease it in very carefully! 

![](images/build diagrams/optics/insert beamsplitter.png)

## Assemble and mount camera module  {pagestep}

First insert a 7 mm disc of the [Laser blocking film](optical/laser_blocking_film.md){qty:1, cat:optics} into the [Camera lens tube](printed/camera_tube_lens.md){qty:1, cat:printed_resin} then the [F7D8 aspherical lens](optical/F7D8_aspherical_lens.md){qty:1, cat:optics} lens on top of the film. Make sure the flatter side of the aspherical lens faces outward.

Next screw the camera lens tube onto the camera module, leaving about 2 mm before it bottoms out.

Next screw the camera module onto the camera mount with 4x [M2.6 self-tapping posi head screws 6 mm](mechanical/screws.yaml#self_tapping_m2.6x6_posi){cat:mechanics, qty:4}. 

Optionally add vertical adjustment to the camera mount as follows:

1. 1x [Stainless steel extension spring, 0.3 mm wire, 20 mm length, 6 mm diameter](mechanical/extension_springs_20x6x0.3mm.md){qty:1, cat:mechanics} in the camera mount between the overhanging tab and the base of the mount.
2. 1x [M3 self-tapping posi head screws 12 mm](mechanical/screws.yaml#self_tapping_m3x12_posi){qty:1, cat:mechanics} through the tab and spring.

The camera mount can now be adjusted slightly up and down by turning the screw.

Finally attach the camera mount to the main body with 2x [M3 self-tapping posi head screws 8 mm](mechanical/screws.yaml#self_tapping_m3x8_posi){qty:2, cat:mechanics} as shown.

![](images/build diagrams/optics/camera assembly.png)
![](images/build diagrams/optics/attach camera assm.png)
![](images/build photos/20260530_153657 cam lens to tube.jpg)
![](images/build photos/20260530_153752 cam tube to module.jpg)
![](images/build photos/20260530_154111 cam module to mount.jpg)
![](images/build photos/20260530_154308 cam mount to main body.jpg)


## Check your assembly

Check that you have everything in the right place according to the images below. (Note detectors and the LED flash tool are described on the next page (electronics).)

![](images/build diagrams/optics/main body with optics - 1s1f annotated.png)
![](images/build diagrams/optics/main body with optics - 2s14f annotated.png)
![](images/build diagrams/optics/main body with optics - 2s14f - perspective.png)
![](images/build photos/20260928_152054 main body fully assembled 2s14f.jpg)
