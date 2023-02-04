# JXSpector
ZX Spectrum and Sega Master System emulator written in Java

What is JXSpector?
------------------

JXSpector is a cross-platform emulator written in Java. It currently emulates a Sinclair ZX Spectrum (48K and 128K models) and the Sega Master System, also known as the Sega Mark III (including a mode to play Game Gear ROMs).

Please consider the currently available version to be very much an early "alpha" version. The purpose of this version is to get some early feedback on gaps in the emulation itself (in particular, on actual software that does not currently run on the emulator). I have a long list of fixes and improvements that will be made to the UI in due course.

Where do I get the latest version of JXSpector from?
----------------------------------------------------

You can get the latest version of JXSpector at any time from its Github repository:

https://github.com/neilcoffey/JXSpector

If you have downloaded JXSpector, please watch this repository to get future updates.

What Spectrum and Master System software can JXSpector run?
-----------------------------------------------------------

JXSpector should run most software unless it requires specific peripherals (e.g. light gun, Interface 1...) that aren't currently supported. As mentioned, part of the reason for this initial release is to gather feedback on software that turns out not to work so that the relevant fixes/support can be added.

Supported features
------------------

ZX Spectrum emulation includes the following features:

- 48K and 128K modes
- Input media formats: .z80, .tap, .tzx, .wav/.aiff
- Output: basic snapshot to .z80 format
- Extra keys: / = Symbol Shift
- Kempston Joystick (arrow keys/control)
- Speaker and AY sound (tone channels only)

Master System emulation includes the following:

- PAL/NTSC timing options
- SMS/Game Gear video modes
- Cartridge save for ROM that support it
- Keys: Joypad 1 - Arrows, Space and Enter; Joypad 2 - O/P/Q/A and /N/M; Game Gear Start/pause - 0
- Standard PSG sound and FM synthesis via Java's built-in soft synth (Gervill)

Prerequisites
-------------

To run JXSpector, you need to have a recent version of the Java Runtime Environment (or Java Development Kit) installed. Specifically, you need Java 17 or later. If your OS does not already have Java installed:

- Sources such as https://adoptium.net offer free distributions for many platforms
- On Linux, your package manager is likely to have Java packages available to install

How do I run the emulator?
--------------------------

JXSpector is currently distributed as a Java Archive file (named JXSpector.jar). There is currenly no "installer" as such: copy JXSpector.jar to a place of your choice and run it from there. You should be able to launch JXSpector in one of two ways:

- On many systems (notably Windows and Mac OS), you can double-click on the JXSpector.jar file to launch the application
- On some systems, you may need to launch the application from the command line:

> cd (place-where-JXSpector-is-installed)

> java -jar JXSpector.jar

On launching the program for the first time, a setup dialog will appear. You will be able to confirm the location of the contents directory where ROM files will be installed and copied to. The application itself remains in the place where you copied it to.

Is there a standard Windows or Mac OS installer, Debian package, RPM etc?
-------------------------------------------------------------------------

These are being worked on for a future version :) For now, you need to run the JXSpector.jar as detailed above.

What missing features are planned next?
---------------------------------------

The following are in the pipeline:

- Key remapping
- SMS snapshot
- Noise and envelope support for AY chip emulation on Spectrum 128
- Z80 debugger
- Additional video export/debug options

Where's the source code?
------------------------

The first source release is planned shortly (under the same BSD license). If you prefer to wait for the source code before running JXSpector, please watch this repo!

Known titles with issues
------------------------

- Desert Speed Trap (SMS): screen corruption and timing issues
