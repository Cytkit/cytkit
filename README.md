# Cytkit
![Cytkit bee mascot](/Presentation%20materials/cytkit_logo_bee_thumb.png)

__Your open-source spectral cytometry sidekick__ 

## Introduction
See the project website at [cytkit.com](https://cytkit.com) to learn about this project. 

Aim: to build a highly useful and accessible cytometry analyser:
- Useful for technology developers and laboratory hackers
- Useful for resource-limited labs
- Useful for teaching flow cytometry
- Useful for all cell biologists

The design is now v1.0 and contains all mechanical parts, an optical model, and a bill of materials. Two configurations are included: Cytkit 1S-1F using entirely off-the-shelf electronics (one scatter, one fluorescence), and Cytkit 2S-14F which uses the 16-channel cytometry electronics set of our spin-out-company Astute Devices.

Please [get in touch](https://cytkit.com/contact) if you are:
- interested in contributing
- interested in buying a kit
- interested in requesting our expertise
- interested in anything else!

## License
This project is released under the CERN Open Hardware Licence Version 2 - Strongly Reciprocal [CERN-OHL-S](https://opensource.org/license/cern-ohl-s). 

That means you can study and modify this design. You may also manufacture and distribute products based on it if you release derivative designs under the same open source license. 

There is no warranty. All liabilities are disclaimed. You accept the design "as is." 

## Specification
Cytkit is intended to be one's personal cytometry _sidekick_:
- Conventional format, but small
- Easy to adjust, align and maintain... no need for a service contract
- Separate sheath and waste bottles
- Volumetric sample pump for absolute concentration measurement of cell populations
- Conventional single SIP-tube sample loader 
- User interface on PC connected by USB
- Can be powered by USB power pack
- Mechanical parts all 3D-printed

![Cytkit bench scene with scientist](/Presentation%20materials/cytkit%20on%20bench%20scene.png)

## Cytometry
The cytometry is based on a single laser plus an spectral array of solid-state detectors.

__Why?__

- Skilled cytometrists can currently measure up to 10 fluorophores on a 488 nm laser alone
- Take advantage of low-cost reagents for the 488 nm laser
- Take advantage of available low-cost parts: SiPMs plus dispersion element rather than many expensive filters
- Such a design can be mechanically simple, allowing fully 3D printed mechanics, simple assembly, adjustment and alignment

## Source files
The full mechanical design has been built with FreeCAD and is provided in [CAD and optical model/Cytkit master assembly.FCStd](/CAD%20and%20optical%20model/Cytkit%20master%20assembly.FCStd)

The optical model has been built in the FreeCAD Optical Design Workbench and is provided in [main body with optics.FCStd](/CAD%20and%20optical%20model/main%20body%20with%20optics.FCStd)

STL files for 3D printing and the Bill of Materials are provided in the build instructions, compiled with Gitbuilding.

## Credits
This project was started by Samson Rogers to bring a low-cost open-source cytometer design to the cytometry community. Oliver Burton has contributing to the specification and built much of the software Honeychrome included many advanced analysis features. Catherine Vant has designed the electronics. The inspiration came from the Open Cytometry Hardware workshop by David Novo at CYTO 2024 in Edinburgh, and also from the OpenFlexure Microscope project led by Richard Bowman. The project is also dedicated to the memory of Howard Shapiro, whose biggest aim was to popularise open cytometry hardware. Thanks to many friends and colleagues for friendly advice!

## Safety
**Note that lasers, such as the one listed in the Bill of Materials are hazardous to the eyes. Direct exposure could cause permanent eye damage. You are strenuously advised to have laser safety training before building your own Cytkit.**