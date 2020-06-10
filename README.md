# FastDOOM
Doom port for DOS, based on PCDoom by @nukeykt. The goal of this port is to make it as fast as posible for 386/486 personal computers.

## FastDOOM vs Original

* Added FPS calculation after timedemo runs
* Removed network gaming support
* Removed joystick support
* Added option to render visplanes (ceiling and floors) without textures. Enable with "-flatsurfaces"
* Added option to render Spectres and invisible objects like real transparent objects (harder to see, faster to render). Enable with "-flatshadows"
* Added option to render sky as a flat color. Enable with "-flatsky"
* Added option (yet to be enabled) to render Spectre and invisible objects like the Sega Saturn port did
* PC Speaker uses all sounds available (just for fun!)
* Lot's of optimizations to make the game run faster / smoother
* Added a basic debug interface, so you can write to a second screen in DOS (MDA, monochrome)
* Removed low memory limit (may cause crashes with low RAM)

## TODO / Nice to have

- [ ] Get more FPS! (assembly, optimizing loops, etc)
- [ ] Add option to remove long dead monsters, as lesser sprites are faster to render
- [ ] Add option to render up to X distance
- [ ] Rewrite sound library (lump cache is not working right, all sounds are being uncached after 0.4 seconds of not being used, which causes major stutters)
- [ ] Add uncapped framerate support (up to 70 fps)
- [ ] Add a realtime performance viewer (FPS, frametime, total R_DrawColumn and R_DrawSpan calls, ...)
- [ ] Add more drawing modes (VESA?, linear VGA?, ...)
- [ ] Optimize drawing engine (reduce number of "outp" calls, avoid redrawing, avoid drawing multiple times single pixels, ...)

## Build instructions

1) Install Open Watcom C version 1.9.
2) Install Turbo Assembler 3.1, which is distributed with Borland C++ 3.1 (1992, not compatible with x64, use DOSBox or a real DOS environment).
3) Add Watcom's bin folder (binnt on Windows, binw on DOS) to the PATH.
4) Run make.bat.

## Contributing

Feel free to add issues or pull requests here on GitHub. I cannot guarantee that I will accept your changes, but feel free to fork the repo and make changes as you see fit. Thanks!
