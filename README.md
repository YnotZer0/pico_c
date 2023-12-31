# pico_c
Raspberyy Pi Pico code / applications

The code is a direct copy from https://github.com/Jean-MarcHarvengt/MCUME
all rights etc.. belong to that chap.

I just got it running / working on a PICOZX using RGB222 as it now gets me all the colours.

https://github.com/YnotZer0/picozx_atari800/blob/main/VID_20231231_153910.mp4

About a year ago, I did attempt this on a PicoVGA https://github.com/pi-gram/pico_c/tree/main/MCUME_pico_picodemo_VGA
however, I did not get the colours working nor a keyboard.

A year later, I believe the code will work on the PicoVGA - if you replace the SDCard code (which I did do before)
I did attempt it, but then spent to much time faffing about distracting myself and besides I had just soldered
the PicoZX board for the ZXSpectrum Pico and I wondered if I could get the Atari-800 emulator from before working on
the PicoZX, meaning I could switch between Spectrum and Atari on the same Pico.

Well, mission accomplished.

One thing I do not have is the ability to use the UI menu to pick the game from the /800 folder, it picks the 2nd file
and loads it auto-magically, which just happens to be Alien Ambush.rom

To remake, copy files from repo and then run:
cd build
cmake -DPICO_BOARD=vgaboard ..
make -j4

the output pico800.uf2 can now be copied to the Pico.

Upon starting on the PicoZX, press the [Menu] button and the debug output will be shown:
new filepath is
800/AlienAmbush.rom
sound buffer allocated
sound initialized
Allocating RAM
Initialising ...
FileSize...
800/AlienAmbush.rom
FileOpen...
800/AlienAmbush.rom
8k
antic
gtia
pia
pokey
6502 reset
init done

I could solder a small screen to the PicoZX and set up the config to see if the menu is output onto that screen rather than the VGA.
