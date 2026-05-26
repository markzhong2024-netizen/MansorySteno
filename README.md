# MansorySteno 
This is a stenography keyboard, but the PCB is masnory (there is also a GitHub for that masnory PCB)
The GitHub for the Mansory PCB for more info is: https://github.com/dcpedit/masonry (the maker of this PCB is dcpedit)

# Ordering the PCB from JLCPCB
First, download the folder (or download the whole zip, then find the production file), then the zip is what you want to upload for the Gerber files. When they ask you for the BOM, upload the files that say BOM and CSV also, and choose the option for assembling the parts, or else they won't ask you for the BOM or the CSV files. Remember to tell JLPCB to assemble the back side, or else they won't find anything to assemble (if you want it explained differently, then check out the Mansory PCB GitHub)

# Supplies
1. Mansory PCB
2. 28 Switches
3. Soldering Iron
4. Solder Wire
5. Mill-Max Hot Swaps (optional)
6. A USB-C to USB-C cable with data

# Firmware
First, download the firmware from the firmware folder. Now, put it in the downloads folder (the command will try to find the file to flash it from the downloads,s so its importent to do that). Now you are going to put the PCB into the bootloader by pressing the boot button, not the reset button. Now your device might ask you if you want to connect to the PCB, click Yes. Then use this command 

For Mac:

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
For Linux:

Install dependencies
```bash
sudo apt install -y git python3-pip
```

Install QMK
```bash
python3 -m pip install qmk
```

Set it up
```bash
qmk setup
```
Flash!
```blash
qmk compile -kb dcpedit/masonry -km steno && qmk flash -kb dcpedit/masonry -km steno
```

For Windows

Go to https://msys.qmk.fm, then download it. Once you have done that and followed all the steps on the official guide https://msys.qmk.fm/guide, you want to run the command 
```bash
qmk setup
```
Then flash it
```bash
qmk compile -kb dcpedit/masonry -km steno && qmk flash -kb dcpedit/masonry -km steno
```

# Plover setup
Go to: https://github.com/opensteno/plover/releases/tag/v5.3.0
