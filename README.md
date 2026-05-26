# MansorySteno 
This is a stenography keyboard, but the PCB is mandatory (there is also a GitHub for that mandatory PCB)
The GitHub for the Mansory PCB for more info is:https://github.com/dcpedit/masonry (the maker of this PCB is dcpedit)

# Ordering the PCB from JLCPCB
First, download the folder (or download the whole zip, then find the production file), then the zip is what you want to upload for the Gerber files. When they ask you for the BOM, upload the files that say BOM and CSV also, and choose the option for assembling the parts, or else they won't ask you for the BOM or the CSV files (if you want it explained differently, then check out the Mansory PCB GitHub)

# Supplies
1. Mansory PCB
2. 28 Switches
3. Soldering Iron
4. Solder Wire
5. Mill-Max Hot Swaps (optional)
6. A USB-C to USB-C cable with data

# Firmware
Note: You will need QMK toolbox to run the commands I will show you, so you will have to download that

First, download the firmware from the firmware folder. Now, put it in the downloads folder (the command will try to find the file to flash it from the downloads,s so its importent to do that). Now you are going to put the PCB into the bootloader by pressing the boot button, not the reset button. Now your device might ask you if you want to connect to the PCB, click Yes. Then use this command 

Mac:
If you don't have Homebrew, install that
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Install the QMK brew so you can use custom commands
```bash
brew install qmk/qmk/qmk
```
Setup QMK
```bash
qmk setup
```
Flash!
```bash
qmk compile -kb dcpedit/masonry -km steno
```
Windows



