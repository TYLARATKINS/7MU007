# 7MU007 PlayStation 3 Drum Machine (WINDOWS)

![alttext](https://i.gyazo.com/e77f15336d616b73d46d3ad725ad8f59.png)

Overview
----------------------------------------------------------------------------

This guide will demonstrate how to turn an old Playstation 3 controller into a fully customisable drum machine. This is done through isolating keyboard input data as code, then converting this data into numbers which then trigger samples in a MaxMSP patch that is included in the directory. This input data is then correlated with specific keys on a computer keyboard and bound to the buttons of the Playstation 3 controller, through the use of two external software’s. The final product can be used to trigger any samples, alongside trigger functions of MaxMSP.

YouTube Video Demo of Project: https://www.youtube.com/watch?v=oAcF640PGU4

What You Will Need
----------------------------------------------------------------------------

1. SCP Toolkit – https://github.com/nefarius/ScpToolkit/releases

2. Joytokey - https://joytokey.net/en/

3. MaxMSP - https://cycling74.com/

4. PS3 controller

5. Patches & Profiles for software (Included in directory)

Instructions
-----------------------------------------------------------------------------

First download and install the SCP Toolkit software, this is a driver to allow the PlayStation 3 controller to be used on a windows computer. This software is typically used to play steam games or emulators without a computer keyboard, but we are only going to need the driver. Connect the PlayStation 3 controller to the computer via USB and follow the installation instructions.

![alttext](https://a.fsdn.com/con/app/proj/scptoolkit.mirror/screenshots/scptoolkit%20driver%20installer.png)

Once installed, download and install ‘Joytokey’ from the link provided. This software allows computer key and mouse input to be assigned to the buttons and control sticks of a USB videogame controller. Load up the software and select ‘preferences’, then ‘configure controllers’, then ‘advanced’, ensure the ‘Xinput1’ controller is selected. As this software does not have the ability to load pre-made CFG files, each key will have to be bound separately. Next select new profile, on the right hand side a window displays all of the assigned keys to the controller, click on each function and bind the following keys;

![alttext](https://i.gyazo.com/9d3c2a8babf6a1ca3e52e58c4c326921.png)

Next, select settings and ‘Associate profile with applications’, then open a notepad file, click on the text editor window and wait for a moment. Joytokey will then recognise this application and allow the use of the controller with it. Test out the controller by hitting some buttons to see if the text file outputs some of the assigned letters. Once this is done, open the included MaxMSP patcher file and repeat the same process to associate the controller with the application. Once this is complete the controller will output the keystrokes to MaxMSP. 

![alttext](https://i.gyazo.com/80e823be1436f5e1cf86c0474d73320f.jpg)

Included MaxMSP patch is a drum sampler, with two kits included in the github directory. To turn the sampler on, click the speaker icon and turn up the output gain to a desired level. Then to load a whole drum kit, select the load sample button. This will prompt a window to open to select some samples for the drum kit. Once each sample has been chosen, hit some of the buttons on the controller and have some fun experimenting with the patterns you can make. 

![alttext](https://i.gyazo.com/08454b86ac5e96e17b79465bae9f94ac.png)

Samples can also be individually loaded and bound to specific buttons, following the key included in the max patch. Unlock the max patch and assign the samples the buttons required by pressing the open message above each sampler. 

Further Development
-----------------------------------------------------------------------------

This project can be adapted to use many other controllers including Xbox, flight simulator joysticks etc., using the equivalent software that enables the controller to have keys bound to it. In relation to adapting the max patch, the data that is output from the [key] object to the [number] object can be used to send a message to any max process. This could result in the manipulation of synthesizer waveforms, to play notes on a controller or control a filer or something similar. This project highlights the potential of old technology that is left around collecting dust in your room or attic.

If you enjoy this project and would like more information, or adapt it into something cooler, please feel free to email me at: tylaratkins@mail.com

Thanks! 
