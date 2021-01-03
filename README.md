# Nutella Tsunami WAV Converter
#### Sample Converter Application for Tsunami WAV Trigger ####

## Summary ##
Ever got upset by the tedious process of converting and renaming sound files for the [Tsunami WAV Trigger](https://www.sparkfun.com/products/13810) board? Well today is your lucky day! This application lets you collect, review and arrange WAV samples in the Tsunami banks, converts them to the required 44.1 kHz / 16bit / No meta-data format, and assigns the filenames according to the [proper naming convention](https://learn.sparkfun.com/tutorials/tsunami-hookup-guide).

## Requirements ##
To use this method for placing WAV files on the SD card of the Tsunami you will need:

- Computer with Microsoft Windows operating system
- Tsunami WAV Trigger
- SD Card
- SD Card reader or adapter
- LabVIEW Run-Time (2019 32-bit) or Development Environment (2019 or later) installed
- This application

## Setting up the environment ##
This application is created using [LabVIEW](https://www.ni.com/hu-hu/shop/labview.html). It uses functionality from the LabVIEW libraries and thus either the [LabVIEW Run-Time Engine](https://knowledge.ni.com/KnowledgeArticleDetails?id=kA03q000000YGvpCAG&l=hu-HU) or the [LabVIEW Development Environment](https://www.ni.com/hu-hu/innovations/videos/10/introduction-to-the-labview-programming-environment.html) must be installed on your computer. If you want to just run the application the Run-Time Engine is enough to have, however to open and edit the VIs you will need the Development environment. Luckily [LabVIEW Community edition](https://www.ni.com/hu-hu/support/downloads/software-products/download.labview-community.html#343639) is [free to use for non-commercial and non-industrial purposes](https://www.ni.com/hu-hu/support/documentation/supplemental/20/labview-community-edition-usage-details.html).
Once the software environment is set up you can either run the application by launching the .exe file or open and edit the project. You only need to install LabVIEW once, any projects or executables can be used afterwards.

### For running the application: ###
1. Download and install the [LabVIEW Run-Time Engine (2019 32-bit)](https://www.ni.com/hu-hu/support/downloads/software-products/download.labview.html#301182) 
2. Download/Clone this repository and run the .exe file 

### For editing the VIs: ###
1. Download and install [LabVIEW Community](https://www.ni.com/hu-hu/support/downloads/software-products/download.labview-community.html#343639)
2. Open the .lvprj file
3. Open the MAIN.VI for the main application
4. Open subVIs to see subVIs  

## How to use this application? ##
The goal was to create a simple and intuitive interface for the program. Do not forget to place and flash the firmware with the .hex file first, and configure the device using the .ini file. See details on the initial configuration [in the user guide](https://robertsonics.com/tsunami-user-guide/).

![alt text](https://raw.githubusercontent.com/drChungus/Nutella-Tsunami-Wav-Converter/main/resources/ui.png)

How to use the application:

1. Select Samples from 1-16
2. Preview Samples (optional)
3. Select Target Folder
4. Set Bank for new samples
5. Click Convert and Place
6. Converted and renamed files will be placed in the target folder.

## Next Steps ##
Some limitation of the current version is:

- Only WAV files are accepted for conversion.
- The app does not check if files with the current indexes already exist in the target folder
- Stereo files can be created, but both channels will be same
- Testing was done using the mono firmware
- You need to use LabVIEW 2019 32-bit Run-Time specifically to run the .exe file. Any version later than 2019 can be used for editing. 


*IMPORTANT: As now you can easily create countless sound banks, I highly recommend using the latest version of the [Tsunami firmware](https://drive.google.com/file/d/1GrqSQpR2VKMzPQoNLvJXjxqHPFFW95dF/view?fbclid=IwAR1-I4ni458oQEHdQdAj23qC7N8M2wlTcuJTn_DnCeNR7ct28mvp-F3CuHc)(v1.11). This is a beta release, but it allows you to have 256 trigger banks. You can find the .hex file and the .ini configurations I used for development and testing in the resources folder.*

**If you experience any bugs or issues feel free to report them using the [Issues](https://github.com/drChungus/Nutella-Tsunami-Wav-Converter/issues) tab!**

*Disclaimer: this is a publicly available beta version and everything is provided as is. No responsibility is taken for bricked devices, lost files or broken SD cards. The likelihood of any of those is minimal, but no extensive testing was done to verify all setups and scenarios.*

